# neops.core.provider.generic_report
## GenericReportProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Excel to Process Tasks


##### Properties


- **`report_for`** *(string)*: Select on which entity you want to report. Must be one of: `['GROUP', 'DEVICE', 'INTERFACE']`.

- **`template`** *(string)*: Jinja template the report.

### Methods
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,report_for: str,template: str,**kwargs) -> Any
```
```python
run_on_device_group(self,device_group_id: int,report_for: str,template: str,**kwargs) -> Any
```
```python
run_on_interface(self,task: nornir.core.task.Task,device_id: int,interface_id: int,report_for: str,template: str,**kwargs) -> Any
```