# neops.core.provider.generic_check_aggregation
## GenericCheckAggregation
Aggregate Check Results to an other entity

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