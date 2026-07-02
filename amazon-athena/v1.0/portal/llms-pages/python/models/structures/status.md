# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXR1cw


# Class Name

`Status`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`QueryExecutionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/query-execution-state-1.md) | Optional | - |
| `state_change_reason` | `str` | Optional | - |
| `submission_date_time` | `datetime` | Optional | - |
| `completion_date_time` | `datetime` | Optional | - |
| `athena_error` | [`AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/athena-error-2.md) | Optional | - |


# Example

```python
import dateutil.parser

from amazonathena.models.athena_error_2 import AthenaError2
from amazonathena.models.query_execution_state_1_enum import QueryExecutionState1Enum
from amazonathena.models.status import Status

status = Status(
    state=QueryExecutionState1Enum.QUEUED,
    state_change_reason='StateChangeReason8',
    submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    athena_error=AthenaError2(
        error_category=3,
        error_type=128,
        retryable=False,
        error_message='ErrorMessage8'
    )
)
```



