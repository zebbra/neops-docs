# neops.core.provider.device_discovery
## DeviceDiscoveryProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Device Discovery


##### Properties


- **`recursive`** *(boolean)*: discover and add neighbors with same credentials as well. Default: `False`.

- **`include_interfaces`** *(boolean)*: discover interfaces of the device. Default: `True`.

- **`include_neighbors`** *(boolean)*: discover neighbors and set edges between devices. Default: `True`.

- **`include_clients`** *(boolean)*: discover network clients and assign to interfaces. Default: `True`.

- **`get_config`** *(boolean)*: get the configuration and update database. Default: `True`.

### Methods
```python
run_on_nornir_device(self,task: nornir.core.task.Task,execute_on: List = None,**kwargs) -> NoneType
```