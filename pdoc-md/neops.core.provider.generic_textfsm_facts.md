# neops.core.provider.generic_textfsm_facts
## GenericTextFSMFacts
Description of the base run cycle for a provider

----------
### JSON Schema
#### Add Structured Command to Facts


##### Properties


- **`facts_key`** *(string)*: Set the key where the facts are saved.

- **`command`** *(string)*: Show command to convert to structured data.

- **`run_on`** *(string)*: Run on Group, Device or Interface. Must be one of: `['DEVICE', 'INTERFACE']`.

- **`add_facts_to`** *(string)*: Add Facts to Group, Device or Interface. Must be one of: `['GROUP', 'DEVICE', 'INTERFACE']`.

- **`jmes_param`** *(string)*: Add a JMES Path that can be uses as Param in the command.
                The $1 will be replaced by the content.
                For executing and parsing the command we expect a list.
                (access to device facts use facts. as initial key). Default: ``.

- **`jmes_interface`** *(string)*: Add a JMES Path to the interface name of the result for the mapping. Default: ``.

- **`textfsm`** *(string)*: TextFSM Template to parse the show output.

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
add_markdown_helptext(self,md_content: neops.core.libs.helptext.markdown_content.MarkDownContent) -> 
```
Creates additional helptext. Make shure the class is instantiable through import_string method
:return: Helptext string

----------
```python
init_adjust_run_on(self,execute_on: Union[List[int], NoneType] = None,execute_on_type: Union[neops.core.provider.base.enum.RunOnEnum, NoneType] = None,dry_run: Union[bool, NoneType] = None,task_input_kwargs: Union[Dict[Any, Any], NoneType] = None,search_query: str = '',task_kwargs: Union[Dict[Any, Any], NoneType] = None,**kwargs) -> NoneType
```
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,**kwargs) -> Any
```