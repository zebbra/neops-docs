# neops.core.provider.deprecated.device_regex_facts
## DeviceRegexFactsProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Add Structured Command to Facts


##### Properties


- **`facts_key`** *(string)*: Set the key where the facts are saved.

- **`command`** *(string)*: Show command to convert to structured data.

- **`regex`** *(string)*: Regular expression.

- **`regex_ignore`** *(boolean)*: Regular expression case sensitive or not. Default: `False`.

- **`regex_multi`** *(boolean)*: Regular expression multiline or not. Default: `False`.

- **`regex_dotall`** *(boolean)*: Dot stands for special characters as well. Default: `False`.

- **`match_keys`** *(array)*: map the matches to keys,
                if multiple (for OR in regex without match use (?:expr1|expr2) ).

  - **Items** *(string)*

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
run_on_device(self,task: nornir.core.task.Task,device_id: int,**kwargs) -> Any
```