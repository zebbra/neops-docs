# neops.core.provider.generic_jinja_check
## GenericJinjaCheckProvider
Description of the base run cycle for a provider

----------
### JSON Schema
#### Generic Jinja Check


##### Properties


- **`check_key`** *(string)*: Set the key where the check is saved.

- **`check_on`** *(string)*: Select on which entity you want save the Check. Must be one of: `['GROUP', 'DEVICE', 'INTERFACE', 'CLIENT ON GROUP', 'CLIENT ON INTERFACE']`.

- **`template`** *(string)*: Default: `{% do neops.set_result(True) %}
{% do neops.set_reason("because") %}`.

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
add_markdown_helptext(self,md_content: neops.core.libs.helptext.markdown_content.MarkDownContent) -> 
```
Creates additional helptext. Make shure the class is instantiable through import_string method
:return: Helptext string

----------
```python
init_adjust_run_on(self,execute_on: Union[List[int], NoneType] = None,execute_on_type: Union[neops.core.provider.base.enum.RunOnEnum, NoneType] = None,dry_run: Union[bool, NoneType] = None,task_input_kwargs: Union[Dict[Any, Any], NoneType] = None,search_query: str = '',task_kwargs: Union[Dict[Any, Any], NoneType] = None,**kwargs) -> NoneType
```
```python
process_global_result(self,result: nornir.core.task.Result = None) -> NoneType
```
Global check are currently not supported..

----------
```python
run_on_client_of_interface(self,task: nornir.core.task.Task,client_id: int,check_on: str,template: str,**kwargs) -> Union[neops.core.provider.base.base_check.NeopsCheckResult, NoneType]
```
```python
run_on_client_of_location(self,client_id: int,check_on: str,template: str,**kwargs) -> Union[neops.core.provider.base.base_check.NeopsCheckResult, NoneType]
```
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,check_on: str,template: str,**kwargs) -> Union[neops.core.provider.base.base_check.NeopsCheckResult, NoneType]
```
```python
run_on_device_group(self,device_group_id: int,check_on: str,template: str,**kwargs) -> Union[neops.core.provider.base.base_check.NeopsCheckResult, NoneType]
```
```python
run_on_interface(self,task: nornir.core.task.Task,interface_id: int,check_on: str,template: str,**kwargs) -> Union[neops.core.provider.base.base_check.NeopsCheckResult, NoneType]
```