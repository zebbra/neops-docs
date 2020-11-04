# neops.core.provider.device_configure_from_jinja
## DeviceJinjaConfigureProvider
```
Description of the base run cycle for a provider
```
----------
### Class variables
- **deprecated**: __bool__
- **description**: __str__
- **execution_updater**: __neops.core.provider.base.execution_updater.ExecutionUpdater__
- **json_schema**: __Dict__
- **provider_type**: __neops.core.provider.base.enum.ProviderTypeEnum__
- **result_writer**: __neops.core.provider.base.base_result_writer.BaseResultWriter__
- **run_input_json_schema**: __Dict__
- **run_on**: __neops.core.provider.base.enum.RunOnEnum__
- **run_on_all_if_empty**: __bool__
- **run_on_strict**: __bool__
- **short_description**: __str__
- **validate_input**: __bool__
### Functions
**inherit_json_schema**(__json_schema: Dict = None__) -> __Dict__
```
Merges JSON Schemas: If this method is called on one of the classes children, then
super().json_schema resolves, else we do a pseudo merge.
:param json_schema:
:return:
```
----------