# neops.core.provider.generic_jinja_check
## GenericJinjaCheckProvider
This Provider is inherited from the `NeopsBaseProvider`, it brings additional functionality to handle checks.

Every Task based on this provider needs a check key where the check result is stored in the database per element.

For providers inherits from this provider the check results are written automatically based on the result set
of the pre- and run methods per element.
It supports check results, boolean values and handels exceptions.

This provider should be the base for check providers. So if you create a new check provider with, either
extend this `NeopsCheckBaseProvider` or a concrete check provider

----------
### Check Result
see below

----------
### JSON Schema
#### Generic Jinja Check


##### Properties


- **`check_key`** *(string)*: Set the key where the check is saved.

- **`check_on`** *(string)*: Select on which entity you want save the Check. Must be one of: `['GROUP', 'DEVICE', 'INTERFACE', 'CLIENT ON GROUP', 'CLIENT ON INTERFACE']`.

- **`template`** *(string)*: Default: `{% do neops.set_result(True) %}
{% do neops.set_reason("because") %}`.

### Methods
```python
run_on_client_of_interface(self,task: nornir.core.task.Task,client_id: int,check_on: str,template: str,**kwargs) -> Union[neops.core.provider.base.base_check.NeopsCheckResult, NoneType]
```
```python
run_on_client_of_location(self,client_id: int,check_on: str,template: str,**kwargs) -> Union[neops.core.provider.base.base_check.NeopsCheckResult, NoneType]
```
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,check_on: str,template: str,**kwargs) -> Union[neops.core.provider.base.base_check.NeopsCheckResult, NoneType]
```
```python
run_on_device_group(self,device_group_id: int,check_on: str,template: str,**kwargs) -> Union[neops.core.provider.base.base_check.NeopsCheckResult, NoneType]
```
```python
run_on_interface(self,task: nornir.core.task.Task,interface_id: int,check_on: str,template: str,**kwargs) -> Union[neops.core.provider.base.base_check.NeopsCheckResult, NoneType]
```