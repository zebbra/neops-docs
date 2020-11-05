# neops.core.provider.generic_jinja_facts
## GenericJinjaFactsProvider
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
run_global(self,task_kwargs: Dict[Any, Any],**kwargs) -> Union[Dict[Any, Any], NoneType]
```
```python
run_on_client_of_interface(self,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,dry_run: bool,task_input_kwargs: Dict[Any, Any],search_query: str,task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,device_id: int,interface_id: int,client_id: int,client_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderClientResult,**kwargs) -> Union[Dict[Any, Any], NoneType]
```
```python
run_on_client_of_location(self,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,dry_run: bool,task_input_kwargs: Dict[Any, Any],search_query: str,task_kwargs: Dict[Any, Any],location_id: int,client_id: int,client_result,**kwargs) -> Union[Dict[Any, Any], NoneType]
```
```python
run_on_device(self,task_input_kwargs: Dict[Any, Any],task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,device_id: int,device_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceResult,**kwargs) -> Union[Dict[Any, Any], NoneType]
```
```python
run_on_device_group(self,device_group_id: int,task_kwargs: Dict[Any, Any],device_group_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceGroupResult,**kwargs) -> Union[Dict[Any, Any], NoneType]
```
```python
run_on_interface(self,task_input_kwargs: Dict[Any, Any],task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,device_id: int,interface_id: int,interface_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderInterfaceResult,**kwargs) -> Union[Dict[Any, Any], NoneType]
```