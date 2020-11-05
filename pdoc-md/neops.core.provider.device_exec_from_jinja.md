# neops.core.provider.device_exec_from_jinja
## DeviceJinjaExecProvider
Description of the base run cycle for a provider

----------
### JSON Schema
#### Device Exec


##### Properties


- **`template`** *(string)*: Jinja Template to generate the configuration.

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
get_operations(self,line) -> 
```
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,**kwargs) -> nornir.core.task.Result
```