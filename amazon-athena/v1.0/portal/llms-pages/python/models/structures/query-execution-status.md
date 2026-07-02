# Query Execution Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdHVz

The completion date, current state, submission time, and state change reason (if applicable) for the query execution.

*This model accepts additional fields of type Any.*


# Class Name

`QueryExecutionStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`QueryExecutionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/query-execution-state-1.md) | Optional | - |
| `state_change_reason` | `str` | Optional | - |
| `submission_date_time` | `datetime` | Optional | - |
| `completion_date_time` | `datetime` | Optional | - |
| `athena_error` | [`AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/athena-error-2.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.athena_error_2 import AthenaError2
from amazonathena.models.query_execution_state_1 import QueryExecutionState1
from amazonathena.models.query_execution_status import QueryExecutionStatus

query_execution_status = QueryExecutionStatus(
    state=QueryExecutionState1.QUEUED,
    state_change_reason='StateChangeReason8',
    submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    athena_error=AthenaError2(
        error_category=3,
        error_type=128,
        retryable=False,
        error_message='ErrorMessage8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



