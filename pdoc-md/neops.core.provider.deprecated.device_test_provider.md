# neops.core.provider.deprecated.device_test_provider
### Module functions
```python
test_sub_sub_task(task: nornir.core.task.Task,res: str) -> nornir.core.task.Result
```
```python
test_sub_task(task: nornir.core.task.Task,res: str) -> nornir.core.task.Result
```
## DeviceTestProvider
Description of the base run cycle for a provider

----------
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