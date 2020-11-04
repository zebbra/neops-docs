# neops.core.provider.base.enum
## ExpandElement
```
An enumeration.
```
----------
### Class variables
- **CLIENTS_ON_INTERFACES**
- **CLIENTS_ON_LOCATIONS**
- **DEVICES**
- **GROUPS**
- **INTERFACES**
- **NORNIR_DEVICES**
### Functions
**intersects**(__list1: List[ExpandElement],list2: List[ExpandElement]__) -> ____
**resolve**(__key: str__) -> __neops.core.provider.base.enum.ExpandElement__
**resolve_for**(__key: str,selection: List[ExpandElement]__) -> __Union[neops.core.provider.base.enum.ExpandElement, NoneType]__
## ProviderTypeEnum
```
An enumeration.
```
----------
### Class variables
- **CHECK**
- **CONFIGURE**
- **EXECUTE**
- **FACTS**
- **NONE**
### Instance variables
- **is_check**
- **is_configure**
- **is_execute**
- **is_facts**
- **is_none**
### Functions
**resolve**(__key: str__) -> __neops.core.provider.base.enum.ProviderTypeEnum__
## RunOnEnum
```
An enumeration.
```
----------
### Class variables
- **CLIENT**
- **DEVICE**
- **GENERIC**
- **GLOBAL**
- **GROUP**
- **INTERFACE**
### Instance variables
- **is_client**
- **is_device**
- **is_generic**
- **is_global**
- **is_group**
- **is_interface**
### Functions
**resolve**(__key: str__) -> __neops.core.provider.base.enum.RunOnEnum__
**resolve_for**(__key: str,selection: List[RunOnEnum]__) -> __Union[neops.core.provider.base.enum.RunOnEnum, NoneType]__