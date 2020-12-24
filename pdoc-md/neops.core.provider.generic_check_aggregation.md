# neops.core.provider.generic_check_aggregation
## GenericCheckAggregation
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
#### Excel to Process Tasks


##### Properties


- **`check_key`** *(string)*: Set the key where the check is saved.

- **`aggregate_from`** *(string)*: Aggregate from entity Type. Must be one of: `['DEVICE', 'INTERFACE']`.

- **`check_key_from`** *(string)*: set the check with the check key to aggregate on. Default: ``.

- **`aggregate_to`** *(string)*: Aggregate to entity Type. Must be one of: `['GROUP', 'DEVICE']`.

- **`percent`** *(integer)*: . Default: `100`.

### Methods
```python
run_on_device(self,device_id: int,aggregate_from: str,aggregate_to: str,check_key_from: str,percent: int = 100,**kwargs) -> Any
```
```python
run_on_device_group(self,device_group_id: int,aggregate_from: str,aggregate_to: str,check_key_from: str,percent: int = 100,**kwargs) -> Any
```