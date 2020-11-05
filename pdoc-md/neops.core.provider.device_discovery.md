# neops.core.provider.device_discovery
## DeviceDiscoveryProvider
Description of the base run cycle for a provider

----------
### JSON Schema
#### Device Discovery


##### Properties


- **`recursive`** *(boolean)*: discover and add neighbors with same credentials as well. Default: `False`.

- **`include_interfaces`** *(boolean)*: discover interfaces of the device. Default: `True`.

- **`include_neighbors`** *(boolean)*: discover neighbors and set edges between devices. Default: `True`.

- **`include_clients`** *(boolean)*: discover network clients and assign to interfaces. Default: `True`.

- **`get_config`** *(boolean)*: get the configuration and update database. Default: `True`.

### Class variables
```python
deprecated: bool
```
```python
description: str
```
```python
execution_updater: neops.core.provider.base.execution_updater.ExecutionUpdater
```
```python
json_schema: Dict
```
```python
provider_type: neops.core.provider.base.enum.ProviderTypeEnum
```
```python
result_writer: neops.core.provider.base.base_result_writer.BaseResultWriter
```
```python
run_input_json_schema: Dict
```
```python
run_on: neops.core.provider.base.enum.RunOnEnum
```
```python
run_on_all_if_empty: bool
```
```python
run_on_strict: bool
```
```python
short_description: str
```
```python
validate_input: bool
```
### Methods
```python
run_on_nornir_device(self,task: nornir.core.task.Task,execute_on: List = None,**kwargs) -> NoneType
```