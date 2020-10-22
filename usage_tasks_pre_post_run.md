# Pre and post run tasks

Neops tasks are specific instances of a [neops provider](https://link), which contain the needed configuration such as **pre** and **post run tasks**.

Neops tasks can be reused in other tasks by setting them as a **pre run** or **post run** task. The task resolver will then find a valid sequence to run the tasks.

## Task sequencing

Consider the case where you want to run two tasks, and perform an integrity check after each.

### Independent tasks

If the tasks are completely independent, you may run them independently:
```mermaid
graph LR
    A[Task 1]
    C[integrity check]
    A --> C
```

And

```mermaid
graph LR
    B[Task 2]
    C[integrity check]
    B --> C
```

### Dependent tasks

However, if you have dependencies between 2 or more task, you can specify pre and post run tasks accordingly. 

Here, a dependency of task 1 and task 2 is configured by setting task 1 as a pre run task of task 2.

```mermaid
graph LR
    A[Task 1]
    B[Task 2]
    C[integrity check]
    A --> B
    B --> C
    A --> C
```

Which will be sequenced by the task resolver as following:

```mermaid
graph LR
    A[Task 1]
    B[Task 2]
    C1[integrity check]
    C2[integrity check]
    A --> C1
    C1 --> B
    B --> C2
```

### Optimize task sequence

Consider an example with pre and post run tasks, similar to the previous. Here, a pre run task is added to task 1 and 2, such that the integrity check is mandatory before a change can occur:

```mermaid
graph LR
    A1[Task 1]
    C[integrity check]
    C -- pre --> A1
    A1 -- post --> C
```

which expands to:

```mermaid
graph LR
    A1[Task 1]
    C11[integrity check]
    C12[integrity check]
    C11 --> A1
    A1 --> C12
```

And

```mermaid
graph LR
    A2[Task 2]
    C[integrity check]
    C[integrity check]
    C -- pre --> A2
    A2 -- post --> C
```
which expands to:

```mermaid
graph LR
    A2[Task 2]
    C21[integrity check]
    C22[integrity check]
    C21 --> A2
    A2 --> C22
```

Setting Task 1 as **pre run task** of Task 2, the following task graph is produced:


```mermaid
graph LR
    A1[Task 1]    
    A2[Task 2]
    C[integrity check]
    C -- pre --> A1
    A1 -- post --> C
    C -- pre --> A2
    A2 -- post --> C
    A1 --> A2
```

which expands to:

```mermaid
graph LR
    A1[Task 1]    
    A2[Task 2]
    C11[integrity check]
    C12[integrity check]
    C11 --> A1
    A1 --> C12
    C21[integrity check]
    C22[integrity check]
    C21 --> A2
    A2 --> C22
    A1 --> A2
```

In this example, a sequencing would result in performing the __integrity check__ two times in a row (as we have 2 tasks and 4 integrity checks):

```mermaid
graph LR
    A1[Task 1]    
    A2[Task 2]
    C11[integrity check]
    C12[integrity check]
    C21[integrity check]
    C22[integrity check]
    C11 -- pre task 1 --> A1
    A1 -- post task 1 --> C12
    C12 --> C21
    C21 -- pre task 2 --> A2
    A2 -- post task 2 --> C22
```

Here, the sequence is optimized, such that no duplicates exist and task definition is fulfilled.

```mermaid
graph LR
    A1[Task 1]    
    A2[Task 2]
    C11[integrity check]
    C12[integrity check]
    C22[integrity check]
    C11 -- pre task 1 --> A1
    A1 -- post task 1 --> C12
    C12 -- pre task 2 --> A2
    A2 -- post task 2 --> C22
```