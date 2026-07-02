# Terminate Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXNwb25zZQ

*This model accepts additional fields of type Any.*


# Class Name

`TerminateSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`SessionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/session-state-1.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.session_state_1 import SessionState1
from amazonathena.models.terminate_session_response import TerminateSessionResponse

terminate_session_response = TerminateSessionResponse(
    state=SessionState1.CREATING,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



