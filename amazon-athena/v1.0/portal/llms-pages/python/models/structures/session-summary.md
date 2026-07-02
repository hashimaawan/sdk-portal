# Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlNlc3Npb25TdW1tYXJ5

Contains summary information about a session.

*This model accepts additional fields of type Any.*


# Class Name

`SessionSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/engine-version-1.md) | Optional | - |
| `notebook_version` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `status` | [`Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/status-3.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.engine_version_1 import EngineVersion1
from amazonathena.models.session_state_1 import SessionState1
from amazonathena.models.session_summary import SessionSummary
from amazonathena.models.status_3 import Status3

session_summary = SessionSummary(
    session_id='SessionId8',
    description='Description6',
    engine_version=EngineVersion1(
        selected_engine_version='SelectedEngineVersion4',
        effective_engine_version='EffectiveEngineVersion6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    notebook_version='NotebookVersion4',
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



