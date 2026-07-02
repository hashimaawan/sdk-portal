# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q


# Class Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state_filter` | [`SessionState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/session-state-3.md) | Optional | - |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `str` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```python
from amazonathena.models.list_sessions_request import ListSessionsRequest
from amazonathena.models.session_state_3_enum import SessionState3Enum

list_sessions_request = ListSessionsRequest(
    work_group='WorkGroup8',
    state_filter=SessionState3Enum.IDLE,
    max_results=100,
    next_token='NextToken6'
)
```



