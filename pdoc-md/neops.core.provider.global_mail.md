# neops.core.provider.global_mail
## GlobalMail
The base neops provider contains all methods and required data processing for a concrete provider.
To create a new provider, either extend this NeopsBaseProvider or a concrete provider

----------
### JSON Schema
#### Mail


##### Properties


- **`include_executor`** *(boolean)*: Default: `False`.

- **`mail_to`** *(string)*: email addresses comma separated. Default: ``.

- **`title`** *(string)*: . Default: ``.

- **`body`** *(string)*: . Default: ``.

- **`as_attachment`** *(string)*: . Default: ``.

- **`attachment_name`** *(string)*: . Default: ``.

- **`zip_attachment`** *(boolean)*: Default: `False`.

- **`mail_from`** *(string)*: . Default: ``.

### Methods
```python
run_global(self,execute_on: List[int],execute_on_type: neops.core.provider.base.enum.RunOnEnum,dry_run: bool,task_input_kwargs: Dict[Any, Any],search_query: str,task_kwargs: Dict[Any, Any],result,**kwargs) -> Any
```