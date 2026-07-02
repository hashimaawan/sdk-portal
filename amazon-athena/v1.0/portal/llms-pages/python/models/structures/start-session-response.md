# Start Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlc3BvbnNl


# Class Name

`StartSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `state` | [`SessionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/session-state-1.md) | Optional | - |


# Example

```python
from amazonathena.models.session_state_1_enum import SessionState1Enum
from amazonathena.models.start_session_response import StartSessionResponse

start_session_response = StartSessionResponse(
    session_id='SessionId6',
    state=SessionState1Enum.DEGRADED
)
```



