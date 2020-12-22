# neops.core.provider.device_rommon_upgrade
## DeviceRommonUpgradeProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Device Upgrade ROMMON


##### Properties


- **`source_url`** *(string)*: from this URL the image will be loaded.

### Methods
```python
run_on_nornir_device(self,task: nornir.core.task.Task,dry_run: bool = True,execute_on: List = None,**kwargs) -> NoneType
```