# neops.core.provider.device_snmp_facts
## DeviceSNMPFactsProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Add Structured Command to Facts


##### Properties


- **`facts_key`** *(string)*: Set the key where the facts are saved.

- **`oidKeyPairs`** *(array)*: Specify which OIDs you would like to store as a fact. The fact key can help you to identify the value later.

  - **Items** *(object)*

    - **`oid`** *(string)*

    - **`key`** *(string)*

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
oid_str_to_tuple(self,oid: str) -> 
```
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,dry_run: bool = True,execute_on: List = None,**kwargs) -> Union[Dict, nornir.core.task.Result]
```