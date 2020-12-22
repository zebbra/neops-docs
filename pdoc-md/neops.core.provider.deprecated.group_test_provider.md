# neops.core.provider.deprecated.group_test_provider
### Module functions
```python
test_sub_sub_task(task: nornir.core.task.Task,res: str) -> nornir.core.task.Result
```
```python
test_sub_task(task: nornir.core.task.Task,res: str) -> nornir.core.task.Result
```
## GroupTestProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Group Test Provider


##### Properties


- **`foo`** *(string)*: Foo Task Form Value.

### Methods
```python
pre_run_global(self,**kwargs) -> Any
```
```python
pre_run_on_device(self,**kwargs) -> Any
```
```python
pre_run_on_device_group(self,**kwargs) -> Any
```
```python
pre_run_on_nornir_device(self,**kwargs) -> Any
```
```python
run_global(self,**kwargs) -> Any
```
```python
run_on_device(self,**kwargs) -> Any
```
```python
run_on_device_group(self,**kwargs) -> Any
```
```python
run_on_interface(self,**kwargs) -> Any
```
```python
run_on_nornir_device(self,**kwargs) -> Any
```