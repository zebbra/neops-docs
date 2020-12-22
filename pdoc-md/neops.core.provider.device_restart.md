# neops.core.provider.device_restart
## DeviceRestartProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### JSON Schema


### Methods
```python
run_on_nornir_device(self,task: nornir.core.task.Task,dry_run: bool = True,execute_on: List = None,**kwargs) -> NoneType
```