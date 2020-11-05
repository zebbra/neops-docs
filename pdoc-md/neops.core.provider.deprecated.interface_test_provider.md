# neops.core.provider.deprecated.interface_test_provider
### Module functions
```python
test_failed_sub_task(task: nornir.core.task.Task,res: str,failed: bool = False) -> nornir.core.task.Result
```
## InterfaceTestProvider
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
set_child_to_failed
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
pre_run_on_interface(self,interface_id,**kwargs) -> Any
```
```python
pre_run_on_nornir_device(self,**kwargs) -> Any
```
```python
run_global(self,**kwargs) -> Any
```
```python
run_on_device(self,device_id,**kwargs) -> Any
```
```python
run_on_device_group(self,device_group_id,**kwargs) -> Any
```
```python
run_on_interface(self,interface_id,**kwargs) -> Any
```
```python
run_on_nornir_device(self,nornir_device_id,**kwargs) -> Any
```
### Functions
```python
inherit_json_schema(json_schema: Dict = None) -> Dict
```
Merges JSON Schemas: If this method is called on one of the classes children, then
super().json_schema resolves, else we do a pseudo merge.
:param json_schema:
:return:

----------