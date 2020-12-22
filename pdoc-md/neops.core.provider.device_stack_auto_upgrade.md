# neops.core.provider.device_stack_auto_upgrade
## DeviceStackAutoUpgradeUnattendedProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Stack Auto Upgrade


##### Properties


- **`reload_on_members`** *(number)*: How long should the process wait till the Stack Members are ready. Default: `1200`.

### Methods
```python
run_on_nornir_device(self,task: nornir.core.task.Task,nornir_device_id: int,dry_run: bool = False,**kwargs) -> Any
```