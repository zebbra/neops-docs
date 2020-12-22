# neops.core.provider.device_configure_from_jinja
## DeviceJinjaConfigureProvider
Provider to configure a device based on a jinja template

----------
### Device Configure Parameters
#### Template

A Jinja Template which is processed before apply the result of this template.

The following parameters are passed to the template processing:
    
* `input`: all inputs from the task run arguments
* `device`: the current device object serialized as dictionary
* `neops`: an object to access the neops entity search engine. See [neops base helper]


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
#### Device Configuration


##### Properties


- **`apply`** *(string)*: Method how to apply the configuration, over cli or copy with scp and merge. Must be one of: `['scp', 'cli', 'scp-startup']`.

- **`slow_device`** *(integer)*: Add a factor for longer wait times for heavy loaded devices. Default: `0`.

- **`template`** *(string)*

### Methods
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,**kwargs) -> nornir.core.task.Result
```
`run_on_device` is called by the run cycle.
\
It generates the configuration with the given input parameters

----------