# List Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1Jlc3BvbnNl


# Class Name

`ListSessionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `str` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `sessions` | [`List[SessionSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/session-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |


# Example

```python
import dateutil.parser

from amazonathena.models.engine_version_1 import EngineVersion1
from amazonathena.models.list_sessions_response import ListSessionsResponse
from amazonathena.models.session_state_1_enum import SessionState1Enum
from amazonathena.models.session_summary import SessionSummary
from amazonathena.models.status_3 import Status3

list_sessions_response = ListSessionsResponse(
    next_token='NextToken2',
    sessions=[
        SessionSummary(
            session_id='SessionId6',
            description='Description4',
            engine_version=EngineVersion1(
                selected_engine_version='SelectedEngineVersion4',
                effective_engine_version='EffectiveEngineVersion6'
            ),
            notebook_version='NotebookVersion6',
            status=Status3(
                start_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                last_modified_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                end_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                idle_since_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                state=SessionState1Enum.TERMINATING
            )
        )
    ]
)
```



