# neops.core.provider.generic_from_excel
## GenericFromExcel
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Excel to Process Tasks


##### Properties


- **`run_as`** *(string)*: Select on which entity the task should run on. Must be one of: `['GLOBAL', 'GROUP', 'DEVICE', 'INTERFACE']`.

- **`header_num`** *(number)*: On which line in the sheet is the header placed. Default: `1`.

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

    - **`task_uniquename`** *(string)*: Set unique task name of task to process (task_id has priority).

    - **`task_main`** *(boolean)*: Include pre and post run tasks in this step. Default: `True`.

    - **`task_template`** *(string)*: parse excel content (given as excel var to jinja) and provide the data structure for the task. Default: `{% do neops.set_params({}) %}`.

### Methods
```python
run_global(self,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,dry_run: bool,task_input_kwargs: Dict[Any, Any],search_query: str,task_kwargs: Dict[Any, Any],result=neops.core.provider.base.result.provider_global_result.ProviderGlobalResult,**kwargs) -> Any
```