# neops.core.provider.generic_test_provider
### Module functions
```python
test_failed_sub_task(task: nornir.core.task.Task,res: str,failed: bool = False) -> nornir.core.task.Result
```
## GenericTestProvider
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Interface Test Provider


##### Properties


- **`run_on`** *(string)*: Run Global or on Group, Device or Interface. Must be one of: `['GLOBAL', 'GROUP', 'DEVICE', 'INTERFACE', 'CLIENT']`.

- **`foo`** *(string)*: Foo Task Form Value.

- **`bar`** *(boolean)*: Bar Task Form Value.

### Class variables
```python
set_child_to_failed
```
### Methods
```python
pre_run_global(self,**kwargs) -> Any
```
```python
pre_run_on_device(self,device_id,**kwargs) -> Any
```
```python
pre_run_on_device_group(self,device_group_id,**kwargs) -> Any
```
```python
pre_run_on_interface(self,interface_id,**kwargs) -> Any
```
```python
pre_run_on_nornir_device(self,nornir_device_id,**kwargs) -> Any
```
```python
run_global(self,**kwargs) -> Any
```
```python
run_on_client_of_interface(self,client_id: int,client_result=neops.core.provider.base.result.coupled_provider_result_types.ProviderClientResult,**kwargs) -> Any
```
```python
run_on_client_of_location(self,client_id: int,client_result=neops.core.provider.base.result.coupled_provider_result_types.ProviderClientResult,**kwargs) -> Any
```
```python
run_on_device(self,device_id,**kwargs) -> Any
```
```python
run_on_device_group(self,device_group_id,**kwargs) -> Any
```
```python
run_on_interface(self,interface_id,**kwargs) -> Any
```
```python
run_on_nornir_device(self,nornir_device_id,**kwargs) -> Any
```