# Get Session Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFNlc3Npb25TdGF0dXNSZXNwb25zZQ

*This model accepts additional fields of type Any.*


# Class Name

`GetSessionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `status` | [`Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/status-3.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.get_session_status_response import GetSessionStatusResponse
from amazonathena.models.session_state_1 import SessionState1
from amazonathena.models.status_3 import Status3

get_session_status_response = GetSessionStatusResponse(
    session_id='SessionId4',
    status=Status3(
        start_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        last_modified_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        end_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        idle_since_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        state=SessionState1.TERMINATING,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



