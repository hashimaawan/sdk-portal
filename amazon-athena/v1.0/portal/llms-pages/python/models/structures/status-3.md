# Status 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXR1czM

*This model accepts additional fields of type Any.*


# Class Name

`Status3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `start_date_time` | `datetime` | Optional | - |
| `last_modified_date_time` | `datetime` | Optional | - |
| `end_date_time` | `datetime` | Optional | - |
| `idle_since_date_time` | `datetime` | Optional | - |
| `state` | [`SessionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/session-state-1.md) | Optional | - |
| `state_change_reason` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.session_state_1 import SessionState1
from amazonathena.models.status_3 import Status3

status_3 = Status3(
    start_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    last_modified_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    end_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    idle_since_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    state=SessionState1.CREATING,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



