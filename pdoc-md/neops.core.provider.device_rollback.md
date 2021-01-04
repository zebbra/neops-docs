# neops.core.provider.device_rollback
## DeviceRollbackProvider
Provider to rollback configuration to version from a given date

----------
### JSON Schema
#### JSON Schema



----------
### Run Input JSON Schema
#### Interface Rollback


##### Properties


- **`rollback_date`** *(string)*

### Methods
```python
pre_run_on_nornir_device(self,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,dry_run: bool,task_input_kwargs: Dict[Any, Any],search_query: str,task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,nornir_device_result,**kwargs) -> Any
```
```python
run_on_nornir_device(self,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,dry_run: bool,task_input_kwargs: Dict[Any, Any],search_query: str,task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,nornir_device_result,**kwargs) -> Any
```