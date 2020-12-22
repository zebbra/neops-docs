# neops.core.provider.interface_configure_from_jinja
## InterfaceJinjaConfigureProvider
This provider extends the NeopsBaseProvider by the functionality of storing configurations (on device results) to the device it self by different apply methods.

This provider should be the base for configuration providers. So if you create a new configuration provider with, either extend this `NeopsConfigureBaseProvider` or a concrete configuration provider

----------
### Global Base Configure Parameters
#### Apply Method

The apply method descripbes how the configuration is written to the device.
    
* `cli`: the configuration is applied directly in the configration mode
* `scp`: the configuration is copied (with scp) as a file to the device and applied with an merge operation
* `scp-startup`: the configuration is copied (with scp) as a file to the device and written to the start up configuration


#### Slow Devices

With the `slow_device` parameter you can specify a delay factor to wait a longer time on responses from slow devices

----------
### JSON Schema
#### Interface Configuration


##### Properties


- **`apply`** *(string)*: Method how to apply the configuration, over cli or copy with scp and merge. Must be one of: `['scp', 'cli', 'scp-startup']`.

- **`slow_device`** *(integer)*: Add a factor for longer wait times for heavy loaded devices. Default: `0`.

- **`template`** *(string)*: Jinja Template to generate the configuration.

### Methods
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,**kwargs) -> nornir.core.task.Result
```