# neops.core.provider.device_upgrade_unattended
## DeviceUpgradeUnattendedProvider
Description of the base run cycle for a provider

----------
### JSON Schema
#### Device Upgrade


##### Properties


- **`source_url`** *(string)*: from this URL the image will be loaded.

- **`vrf`** *(string)*: VRF where we should copy. Default: ``.

- **`models`** *(array)*: This description is used as a help message.

  - **Items** *(object)*

    - **`model_regex`** *(string)*: Default: `^$`.

    - **`image`** *(string)*: from this URL the image will be loaded.

    - **`md5`** *(string)*: MD5 sum to verify. Default: ``.

    - **`min_space`** *(integer)*: minimum file size required. Default: `0`.

    - **`overwrite`** *(boolean)*: overwrite image if file exists on device. Default: `False`.

    - **`restart`** *(boolean)*: restart device when image is copied and installed. Default: `False`.

    - **`save_config_if_required`** *(boolean)*: Save config before restart if asked so. Default: `True`.

    - **`reload_wait_time`** *(number)*: How long should the process wait at reload after upgrade. Default: `1200`.

### Class variables
```python
deprecated: bool
```
```python
description: str
```
```python
execution_updater: neops.core.provider.base.execution_updater.ExecutionUpdater
```
```python
json_schema: Dict
```
```python
provider_type: neops.core.provider.base.enum.ProviderTypeEnum
```
```python
result_writer: neops.core.provider.base.base_result_writer.BaseResultWriter
```
```python
run_input_json_schema: Dict
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
```python
validate_input: bool
```
### Methods
```python
add_markdown_helptext(self,md_content: neops.core.libs.helptext.markdown_content.MarkDownContent) -> 
```
Creates additional helptext. Make shure the class is instantiable through import_string method
:return: Helptext string

----------
```python
run_on_nornir_device(self,task: nornir.core.task.Task,nornir_device_id: int,**kwargs) -> Any
```