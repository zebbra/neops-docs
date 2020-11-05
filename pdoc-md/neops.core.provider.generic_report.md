# neops.core.provider.generic_report
## GenericReportProvider
Description of the base run cycle for a provider

----------
### JSON Schema
#### Excel to Process Tasks


##### Properties


- **`report_for`** *(string)*: Select on which entity you want to report. Must be one of: `['GROUP', 'DEVICE', 'INTERFACE']`.

- **`template`** *(string)*: Jinja template the report.

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
init_adjust_run_on(self,report_for: str,**kwargs) -> NoneType
```
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,report_for: str,template: str,**kwargs) -> Any
```
```python
run_on_device_group(self,device_group_id: int,report_for: str,template: str,**kwargs) -> Any
```
```python
run_on_interface(self,task: nornir.core.task.Task,device_id: int,interface_id: int,report_for: str,template: str,**kwargs) -> Any
```