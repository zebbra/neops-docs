# neops.core.provider.generic_rest_facts
## GenericRestFactsProvider
Description of the base run cycle for a provider

----------
### JSON Schema
#### Add Return Value from REST call to Facts


##### Properties


- **`facts_key`** *(string)*: Set the key where the facts are saved.

- **`url`** *(string)*: Jinja Template can be used to get parameters, element of run on is passed to Jinja Template.

- **`request_on`** *(string)*: Run Global or on Group, Device or Interface. Must be one of: `['GLOBAL', 'GROUP', 'DEVICE', 'INTERFACE']`.

- **`auth`** *(object)*

- **`mapping`** *(object)*

  - **`add_facts_to`** *(string)*: Add Facts to Group, Device or Interface. Must be one of: `['GROUP', 'DEVICE', 'INTERFACE']`.

  - **`mapping_template`** *(string)*: Return string from Jinja Template is evaluated and mapped to given element. Default: `{% do neops.set_facts(response) %}`.

- **`headers`** *(array)*

  - **Items** *(object)*

    - **`header_name`** *(string)*

    - **`header_value`** *(string)*

### Class variables
```python
description: str
```
```python
json_schema: Dict[str, Any]
```
```python
provider_type: neops.core.provider.base.enum.ProviderTypeEnum
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
### Methods
```python
get_rest(self,url: str,auth: Dict = None,headers: List = None) -> Dict
```
```python
init_adjust_run_on(self,execute_on: Union[List[int], NoneType] = None,execute_on_type: Union[neops.core.provider.base.enum.RunOnEnum, NoneType] = None,dry_run: Union[bool, NoneType] = None,task_input_kwargs: Union[Dict[Any, Any], NoneType] = None,search_query: str = '',task_kwargs: Union[Dict[Any, Any], NoneType] = None,**kwargs) -> NoneType
```
```python
pre_run_global(self,request_on: str,url: str,task_input_kwargs: Dict,auth: Dict = None,headers: List = None,**kwargs) -> Any
```
```python
pre_run_on_device(self,task: nornir.core.task.Task,device_id: int,request_on: str,url: str,task_input_kwargs: Dict,auth: Dict = None,headers: List = None,**kwargs) -> Any
```
```python
pre_run_on_device_group(self,device_group_id: int,request_on: str,url: str,task_input_kwargs: Dict,auth: Dict = None,headers: List = None,**kwargs) -> Any
```
```python
pre_run_on_interface(self,task: nornir.core.task.Task,interface_id: int,request_on: str,url: str,task_input_kwargs: Dict,auth: Dict = None,headers: List = None,**kwargs) -> Any
```
```python
run_global(self,result: neops.core.provider.base.result.provider_result.ProviderResult,request_on: str,mapping: Dict,**kwargs) -> Any
```
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,device_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceResult,request_on: str,mapping: Dict,task_input_kwargs: Dict,**kwargs) -> Any
```
```python
run_on_device_group(self,device_group_id: int,device_group_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceGroupResult,request_on: str,mapping: Dict,task_input_kwargs: Dict,**kwargs) -> Any
```
```python
run_on_interface(self,task: nornir.core.task.Task,interface_id: int,interface_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderInterfaceResult,request_on: str,mapping: Dict,task_input_kwargs: Dict,**kwargs) -> Any
```