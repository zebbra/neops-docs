# neops.core.provider.generic_simple_workflow
## GenericSimpleWorkflow
Description of the base run cycle for a provider

----------
### JSON Schema
#### Excel to Process Tasks


##### Properties


- **`run_as`** *(string)*: Select on which entity the task should run on. Must be one of: `['GLOBAL', 'GROUP', 'DEVICE', 'INTERFACE']`.

- **`tasks`** *(array)*: This description is used as a help message.

  - **Items** *(object)*

    - **`titleProp`** *(string)*

    - **`run_as`** *(string)*: Select on which execute on entities will be passed to the task. Must be one of: `['GROUP', 'DEVICE', 'INTERFACE']`.

    - **`allow_all`** *(boolean)*: some providers have the ability to run on all elements if there are none given, decide if this is fine for your task. Default: `False`.

    - **`entity_template`** *(string)*: Get a List of Entity by the Template. Default: `{% set device_list = [] %}
{% for device in neops.search_devices("devices.hostname: *.neops.io") %}
    {{ device.hostname }}
    {% do device_list.append(device.id) %}
{% endfor %}
{% do neops.set_entities(device_list) %}`.

    - **`task_id`** *(number)*: Default: `0`.

    - **`task_template`** *(string)*: parse excel content (given as excel var to jinja) and provide the data structure for the task. Default: `{% do neops.set_params({}) %}`.

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
run_global(self,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,dry_run: bool,task_input_kwargs: Dict[Any, Any],search_query: str,task_kwargs: Dict[Any, Any],result=neops.core.provider.base.result.provider_global_result.ProviderGlobalResult,**kwargs) -> Any
```