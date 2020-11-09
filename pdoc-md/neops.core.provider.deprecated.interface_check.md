# neops.core.provider.deprecated.interface_check
## InterfaceCheckProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

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
run_on_interface(self,interface_id,task,**kwargs) -> Any
```