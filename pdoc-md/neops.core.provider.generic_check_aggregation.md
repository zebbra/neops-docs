# neops.core.provider.generic_check_aggregation
## GenericCheckAggregation
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Excel to Process Tasks


##### Properties


- **`check_key`** *(string)*: Set the key where the check is saved.

- **`aggregate_from`** *(string)*: Aggregate from entity Type. Must be one of: `['DEVICE', 'INTERFACE']`.

- **`check_key_from`** *(string)*: set the check with the check key to aggregate on. Default: ``.

- **`aggregate_to`** *(string)*: Aggregate to entity Type. Must be one of: `['GROUP', 'DEVICE']`.

- **`percent`** *(integer)*: . Default: `100`.

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
run_on_device(self,device_id: int,aggregate_from: str,aggregate_to: str,check_key_from: str,percent: int = 100,**kwargs) -> Any
```
```python
run_on_device_group(self,device_group_id: int,aggregate_from: str,aggregate_to: str,check_key_from: str,percent: int = 100,**kwargs) -> Any
```