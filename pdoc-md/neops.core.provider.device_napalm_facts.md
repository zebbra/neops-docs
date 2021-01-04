# neops.core.provider.device_napalm_facts
## DeviceNapalmFacts
Get napalm facts from a device

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