# neops.core.provider.generic_rest_facts
## GenericRestFactsProvider
Description of the base run cycle for a provider

----------
### Class variables
```python
description: str
```
```python
json_schema: Dict[str, Any]
```
```python
provider_type: neops.core.provider.base.enum.ProviderTypeEnum
```
```python
run_on: neops.core.provider.base.enum.RunOnEnum
```
```python
run_on_all_if_empty: bool
```
```python
run_on_strict: bool
```
```python
short_description: str
```
### Functions
```python
inherit_json_schema(json_schema: Dict = None) -> Dict
```
Merges JSON Schemas: If this method is called on one of the classes children, then
super().json_schema resolves, else we do a pseudo merge.
:param json_schema:
:return:

----------