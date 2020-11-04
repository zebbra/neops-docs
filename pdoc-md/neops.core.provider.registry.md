# neops.core.provider.registry
### Module functions
**get_provider**(__name: str__) -> __Union[Dict, NoneType]__
**get_providers**(____) -> ____
**register_provider**(__cls__) -> ____
```
Register a neops provider. Tasks can be registered for specific vendors and (also optional) specific models.
This decorator only adds a marker attribute on the function, the provider_loader.load_providers function builds the
actual registry. This way we can enforce the correct order of the tasks (default builtin neops providers, after that
all tasks loaded from the NEOPS_PROVIDER_MODULES), and do not depend on the import order of the modules.
```
----------