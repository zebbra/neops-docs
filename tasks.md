# Tasks

neops.io tasks are performing actions (collecting facts, make changes, interact with peripheral systems).

There are currently 4 types of tasks implemented

- CONFIGURE - _configure network devices_
- FACTS - _collecting facts_
- CHECK - _check states based on facts_
- EXECUTE - _generic task for troubleshooting purpose, interact with peripheral systems (if it's not related to facts) or others_

All Tasks are based on [providers](#providers) that execute the tasks. A task is a parameterized provider instance.

## Generic task parameters

Generic task parameters are used to describe the task itself and how it is acting.

### Description

Set an appropriate Description to the task, that describe its functionality.

### Provider name and module

This is a reference to the provider that is used to instantiate and run the task.

### Input parameters (JSON scheme for running the task)

This describes additional input parameters as [JSON Schema](https://json-schema.org/learn/getting-started-step-by-step.html). They are required to run a task.

Before executing a task, a web Form is rendered based on the task JSON schema to get the required input values.

For more information how to build such a JSON Schema look in [Appendix under JSON Form](appendix.md#json-form)

### Pre and post running tasks

For some tasks, like configurations or checks, it's essential to have accurate (actual) data. They are based on current facts or states, which should be collected in front of the task. Such supporting tasks can be referenced as pre- or post-running tasks

**Other parameters are provider specific**
