# Get Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXNwb25zZQ


# Class Name

`GetSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `work_group` | `str` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `engine_version` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `engine_configuration` | [`EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/engine-configuration-1.md) | Optional | - |
| `notebook_version` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `session_configuration` | [`SessionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/session-configuration-2.md) | Optional | - |
| `status` | [`Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/status-3.md) | Optional | - |
| `statistics` | [`Statistics3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/statistics-3.md) | Optional | - |


# Example

```python
from amazonathena.models.additional_configs import AdditionalConfigs
from amazonathena.models.engine_configuration_1 import EngineConfiguration1
from amazonathena.models.get_session_response import GetSessionResponse

get_session_response = GetSessionResponse(
    session_id='SessionId6',
    description='Description4',
    work_group='WorkGroup4',
    engine_version='EngineVersion8',
    engine_configuration=EngineConfiguration1(
        max_concurrent_dpus=94,
        coordinator_dpu_size=1,
        default_executor_dpu_size=1,
        additional_configs=AdditionalConfigs()
    )
)
```



