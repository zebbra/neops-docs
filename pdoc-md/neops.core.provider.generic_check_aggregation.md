# neops.core.provider.generic_check_aggregation
## GenericCheckAggregation
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
init_adjust_run_on(self,execute_on: Union[List[int], NoneType] = None,execute_on_type: Union[neops.core.provider.base.enum.RunOnEnum, NoneType] = None,dry_run: Union[bool, NoneType] = None,task_input_kwargs: Union[Dict[Any, Any], NoneType] = None,search_query: str = '',task_kwargs: Union[Dict[Any, Any], NoneType] = None,**kwargs) -> NoneType
```
```python
process_global_result(self,result: nornir.core.task.Result = None) -> NoneType
```
Global check are currently not supported..

----------
```python
run_on_device(self,device_id: int,aggregate_from: str,aggregate_to: str,check_key_from: str,percent: int = 100,**kwargs) -> Any
```
```python
run_on_device_group(self,device_group_id: int,aggregate_from: str,aggregate_to: str,check_key_from: str,percent: int = 100,**kwargs) -> Any
```