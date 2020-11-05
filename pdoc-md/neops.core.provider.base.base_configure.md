# neops.core.provider.base.base_configure
## NeopsConfigureBaseProvider
Description of the base run cycle for a provider

----------
### JSON Schema
#### Configure Base Provider


##### Properties


- **`apply`** *(string)*: Method how to apply the configuration, over cli or copy with scp and merge. Must be one of: `['scp', 'cli', 'scp-startup']`.

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
success_message
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
run_on_nornir_device(self,task: nornir.core.task.Task,nornir_device_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderNornirDeviceResult,dry_run: bool = True,**kwargs) -> str
```