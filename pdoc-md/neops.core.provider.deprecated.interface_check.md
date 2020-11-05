# neops.core.provider.deprecated.interface_check
## InterfaceCheckProvider
Description of the base run cycle for a provider

----------
### JSON Schema
#### Check Interface Facts with Regex


##### Properties


- **`check_key`** *(string)*: Set the key where the check is saved.

- **`checks`** *(array)*: This description is used as a help message.

  - **Items** *(object)*

    - **`element`** *(object)*

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
process_global_result(self,result: nornir.core.task.Result = None) -> NoneType
```
Global check are currently not supported..

----------
```python
run_on_interface(self,interface_id,task,**kwargs) -> Any
```