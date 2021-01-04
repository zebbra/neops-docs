# neops.core.provider.generic_ping
## GenericPing
Ping Targets and save results as facts

----------
### JSON Schema
#### Add Structured Command to Facts


##### Properties


- **`facts_key`** *(string)*: Set the key where the facts are saved.

- **`add_facts_to`** *(string)*: Add Facts to Group, Device, Interface or Clients. Must be one of: `['GLOBAL', 'GROUP', 'CLIENT OF LOCATIONS', 'DEVICE', 'INTERFACE', 'CLIENT OF INTERFACE']`.

- **`destination_template`** *(string)*: List of Targets (1 per line). Default: `8.8.8.8`.

### Methods
```python
run_global(self,task_kwargs: Dict[Any, Any],**kwargs) -> Union[Dict[Any, Any], NoneType]
```
```python
run_on_client_of_interface(self,task_input_kwargs: Dict[Any, Any],task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,device_id: int,interface_id: int,client_id: int,client_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderClientResult,**kwargs) -> Any
```
```python
run_on_client_of_location(self,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,dry_run: bool,task_input_kwargs: Dict[Any, Any],search_query: str,task_kwargs: Dict[Any, Any],location_id: int,client_id: int,client_result,**kwargs) -> Any
```
```python
run_on_device(self,task_input_kwargs: Dict[Any, Any],task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,device_id: int,device_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceResult,**kwargs) -> Any
```
```python
run_on_device_group(self,device_group_id: int,task_kwargs: Dict[Any, Any],device_group_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderDeviceGroupResult,**kwargs) -> Union[Dict[Any, Any], NoneType]
```
```python
run_on_interface(self,task_input_kwargs: Dict[Any, Any],task_kwargs: Dict[Any, Any],task: nornir.core.task.Task,nornir_device_id: int,device_id: int,interface_id: int,interface_result: neops.core.provider.base.result.coupled_provider_result_types.ProviderInterfaceResult,**kwargs) -> Any
```