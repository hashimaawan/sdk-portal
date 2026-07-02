# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state_filter` | [`SessionState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/session-state-3.md) | Optional | - |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `str` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_sessions_request import ListSessionsRequest
from amazonathena.models.session_state_3 import SessionState3

list_sessions_request = ListSessionsRequest(
    work_group='WorkGroup8',
    state_filter=SessionState3.IDLE,
    max_results=100,
    next_token='NextToken6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



