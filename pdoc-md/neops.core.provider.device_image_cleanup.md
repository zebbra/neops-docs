# neops.core.provider.device_image_cleanup
## DeviceImageCleanUpProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### JSON Schema


### Methods
```python
run_on_nornir_device(self,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,dry_run: bool,task_input_kwargs: Dict[Any, Any],search_query: str,task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,nornir_device_result=neops.core.provider.base.result.coupled_provider_result_types.ProviderNornirDeviceResult,**kwargs) -> Any
```