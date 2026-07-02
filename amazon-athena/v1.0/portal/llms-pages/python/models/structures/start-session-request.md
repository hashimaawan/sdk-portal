# Start Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlcXVlc3Q


# Class Name

`StartSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `work_group` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `engine_configuration` | [`EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/engine-configuration-1.md) | Required | - |
| `notebook_version` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `session_idle_timeout_in_minutes` | `int` | Optional | **Constraints**: `>= 1`, `<= 480` |
| `client_request_token` | `str` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |


# Example

```python
from amazonathena.models.additional_configs import AdditionalConfigs
from amazonathena.models.engine_configuration_1 import EngineConfiguration1
from amazonathena.models.start_session_request import StartSessionRequest

start_session_request = StartSessionRequest(
    work_group='WorkGroup4',
    engine_configuration=EngineConfiguration1(
        max_concurrent_dpus=94,
        coordinator_dpu_size=1,
        default_executor_dpu_size=1,
        additional_configs=AdditionalConfigs()
    ),
    description='Description6',
    notebook_version='NotebookVersion6',
    session_idle_timeout_in_minutes=78,
    client_request_token='ClientRequestToken6'
)
```



