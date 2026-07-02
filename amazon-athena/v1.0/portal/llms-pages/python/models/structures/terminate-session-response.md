# Terminate Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXNwb25zZQ


# Class Name

`TerminateSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`SessionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/session-state-1.md) | Optional | - |


# Example

```python
from amazonathena.models.session_state_1_enum import SessionState1Enum
from amazonathena.models.terminate_session_response import TerminateSessionResponse

terminate_session_response = TerminateSessionResponse(
    state=SessionState1Enum.CREATING
)
```



