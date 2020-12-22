# neops.core.provider.generic_textfsm_facts
## GenericTextFSMFacts
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

- **`command`** *(string)*: Show command to convert to structured data.

- **`run_on`** *(string)*: Run on Group, Device or Interface. Must be one of: `['DEVICE', 'INTERFACE']`.

- **`add_facts_to`** *(string)*: Add Facts to Group, Device or Interface. Must be one of: `['GROUP', 'DEVICE', 'INTERFACE']`.

- **`jmes_param`** *(string)*: Add a JMES Path that can be uses as Param in the command.
                The $1 will be replaced by the content.
                For executing and parsing the command we expect a list.
                (access to device facts use facts. as initial key). Default: ``.

- **`jmes_interface`** *(string)*: Add a JMES Path to the interface name of the result for the mapping. Default: ``.

- **`textfsm`** *(string)*: TextFSM Template to parse the show output.

- **`slow_device`** *(integer)*: Add a factor for longer wait times for heavy loaded devices. Default: `0`.

### Methods
```python
run_on_device(self,task: nornir.core.task.Task,device_id: int,**kwargs) -> Any
```