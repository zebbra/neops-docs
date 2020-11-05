# neops.core.provider.base.base_check
## NeopsCheckBaseProvider
Description of the base run cycle for a provider

----------
### Class variables
```python
based_on_checks
```
```python
check_for
```
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
related_facts
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
process_client_results(self,results: List[neops.core.provider.base.result.coupled_provider_result_types.ProviderClientResult] = None) -> NoneType
```
```python
process_device_group_results(self,results: List[neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceGroupResult] = None) -> NoneType
```
```python
process_device_results(self,results: List[neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceResult] = None) -> NoneType
```
```python
process_global_result(self,result: nornir.core.task.Result = None) -> NoneType
```
Global check are currently not supported..

----------
```python
process_interface_results(self,results: List[neops.core.provider.base.result.coupled_provider_result_types.ProviderInterfaceResult] = None) -> NoneType
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
## NeopsCheckResult
### Class variables
```python
metrics
```
```python
reason
```
```python
result
```