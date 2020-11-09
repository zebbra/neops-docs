# neops.core.provider.generic_textfsm_facts_v2
## GenericTextFSMFactsV2
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Add Structured Command to Facts


##### Properties


- **`facts_key`** *(string)*: Set the key where the facts are saved.

- **`add_facts_to`** *(string)*: Add Facts to Group, Device, Interface or Clients. Must be one of: `['GLOBAL', 'GROUP', 'DEVICE', 'INTERFACE', 'CLIENT']`.

- **`command_template`** *(string)*: Show command to convert to structured data (Jinja is parsed to create the command). Default: `show version`.

- **`textfsm_template`** *(string)*: TextFSM Template to parse the show output.

- **`mapping_template`** *(string)*: parse excel content (given as excel var to jinja) and provide the data structure for the task. Default: `{#### element props group, device, interface or client #}
{#### command results are under the variable command_results #}
{% do neops.set_facts(textfsm) %}`.

- **`slow_device`** *(integer)*: Add a factor for longer wait times for heavy loaded devices. Default: `0`.

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
pre_run_on_nornir_device(self,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,**kwargs) -> Any
```
```python
run_global(self,task_kwargs: Dict[Any, Any],**kwargs) -> Union[Dict[Any, Any], NoneType]
```
```python
run_on_client_of_interface(self,task_input_kwargs: Dict[Any, Any],task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,device_id: int,interface_id: int,client_id: int,client_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderClientResult,**kwargs) -> Any
```
```python
run_on_device(self,task_input_kwargs: Dict[Any, Any],task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,device_id: int,device_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceResult,**kwargs) -> Any
```
```python
run_on_device_group(self,device_group_id: int,task_kwargs: Dict[Any, Any],device_group_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceGroupResult,**kwargs) -> Union[Dict[Any, Any], NoneType]
```
```python
run_on_interface(self,task_input_kwargs: Dict[Any, Any],task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,device_id: int,interface_id: int,interface_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderInterfaceResult,**kwargs) -> Any
```