# neops.core.provider.device_napalm_facts
## DeviceNapalmFacts
This Provider is inherited from the `NeopsBaseProvider`, it brings additional functionality to handle facts (flexible data structures per entity).

Every task based on this provider needs a facts key where the facts result is stored in the database per element.

For providers inherits from this provider the facts results are written automatically based on the result set of the pre- and run methods per element.
It supports data structures of any kind as long as they are compatible to JSON.

This provider should be the base for fact providers. So if you create a new fact provider with, either extend this `NeopsFactsBaseProvider` or a concrete fact provider

----------
### JSON Schema
#### Add Structured Command to Facts


##### Properties


- **`facts_key`** *(string)*: Set the key where the facts are saved.

- **`napalm_fact`** *(string)*: Element to get facts from napalm.

### Methods
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,execute_on: List = None,**kwargs) -> Any
```