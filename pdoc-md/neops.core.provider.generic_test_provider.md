# neops.core.provider.generic_test_provider
### Module functions
```python
test_failed_sub_task(task: nornir.core.task.Task,res: str,failed: bool = False) -> nornir.core.task.Result
```
## GenericTestProvider
Description of the base run cycle for a provider

----------
### JSON Schema
#### Interface Test Provider


##### Properties


- **`run_on`** *(string)*: Run Global or on Group, Device or Interface. Must be one of: `['GLOBAL', 'GROUP', 'DEVICE', 'INTERFACE', 'CLIENT']`.

- **`foo`** *(string)*: Foo Task Form Value.

- **`bar`** *(boolean)*: Bar Task Form Value.

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
add_markdown_helptext(self,md_content: neops.core.libs.helptext.markdown_content.MarkDownContent) -> 
```
Creates additional helptext. Make shure the class is instantiable through import_string method
:return: Helptext string

----------
```python
init_adjust_run_on(self,execute_on: Union[List[int], NoneType] = None,execute_on_type: Union[neops.core.provider.base.enum.RunOnEnum, NoneType] = None,dry_run: Union[bool, NoneType] = None,task_input_kwargs: Union[Dict[Any, Any], NoneType] = None,search_query: str = '',task_kwargs: Union[Dict[Any, Any], NoneType] = None,**kwargs) -> NoneType
```
```python
pre_run_global(self,**kwargs) -> Any
```
```python
pre_run_on_device(self,device_id,**kwargs) -> Any
```
```python
pre_run_on_device_group(self,device_group_id,**kwargs) -> Any
```
```python
pre_run_on_interface(self,interface_id,**kwargs) -> Any
```
```python
pre_run_on_nornir_device(self,nornir_device_id,**kwargs) -> Any
```
```python
run_global(self,**kwargs) -> Any
```
```python
run_on_client_of_interface(self,client_id: int,client_result=neops.core.provider.base.result.coupled_provider_result_types.ProviderClientResult,**kwargs) -> Any
```
```python
run_on_client_of_location(self,client_id: int,client_result=neops.core.provider.base.result.coupled_provider_result_types.ProviderClientResult,**kwargs) -> Any
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