# neops.core.provider.device_exec_from_jinja
## DeviceJinjaExecProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Device Exec


##### Properties


- **`template`** *(string)*: Jinja Template to generate the configuration.

### Methods
```python
get_operations(self,line) -> 
```
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,**kwargs) -> nornir.core.task.Result
```