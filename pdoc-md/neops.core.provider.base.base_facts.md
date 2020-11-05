# neops.core.provider.base.base_facts
## NeopsFactsBaseProvider
Description of the base run cycle for a provider

----------
### JSON Schema
#### Facts Base Provider


##### Properties


- **`facts_key`** *(string)*: Set the key where the facts are saved.

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
facts_for
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
process_client_results(self,results: List[neops.core.provider.base.result.coupled_provider_result_types.ProviderClientResult]) -> NoneType
```
```python
process_device_group_results(self,results: List[neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceGroupResult]) -> NoneType
```
```python
process_device_results(self,results: List[neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceResult]) -> NoneType
```
```python
process_global_result(self,result: neops.core.provider.base.result.provider_result.ProviderResult) -> NoneType
```
```python
process_interface_results(self,results: List[neops.core.provider.base.result.coupled_provider_result_types.ProviderInterfaceResult]) -> NoneType
```