# neops.core.provider.generic_rest_facts
## GenericRestFactsProvider
This Provider is inherited from the `NeopsBaseProvider`, it brings additional functionality to handle facts (flexible data structures per entity).

Every task based on this provider needs a facts key where the facts result is stored in the database per element.

For providers inherits from this provider the facts results are written automatically based on the result set of the pre- and run methods per element.
It supports data structures of any kind as long as they are compatible to JSON.

This provider should be the base for fact providers. So if you create a new fact provider with, either extend this `NeopsFactsBaseProvider` or a concrete fact provider

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

### Methods
```python
get_rest(self,url: str,auth: Dict = None,headers: List = None) -> Dict
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