# neops.core.provider.generic_rest_facts
## GenericRestFactsProvider
```
Description of the base run cycle for a provider
```
----------
### Class variables
- **description**: __str__
- **json_schema**: __Dict[str, Any]__
- **provider_type**: __neops.core.provider.base.enum.ProviderTypeEnum__
- **run_on**: __neops.core.provider.base.enum.RunOnEnum__
- **run_on_all_if_empty**: __bool__
- **run_on_strict**: __bool__
- **short_description**: __str__
### Functions
**inherit_json_schema**(__json_schema: Dict = None__) -> __Dict__
```
Merges JSON Schemas: If this method is called on one of the classes children, then
super().json_schema resolves, else we do a pseudo merge.
:param json_schema:
:return:
```
----------