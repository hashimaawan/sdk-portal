# List Calculation Executions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXNwb25zZQ

*This model accepts additional fields of type Any.*


# Class Name

`ListCalculationExecutionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `str` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `calculations` | [`List[CalculationSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/calculation-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.calculation_execution_state_1 import CalculationExecutionState1
from amazonathena.models.calculation_summary import CalculationSummary
from amazonathena.models.list_calculation_executions_response import ListCalculationExecutionsResponse
from amazonathena.models.status_1 import Status1

list_calculation_executions_response = ListCalculationExecutionsResponse(
    next_token='NextToken2',
    calculations=[
        CalculationSummary(
            calculation_execution_id='CalculationExecutionId0',
            description='Description2',
            status=Status1(
                submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                state=CalculationExecutionState1.CANCELING,
                state_change_reason='StateChangeReason8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        CalculationSummary(
            calculation_execution_id='CalculationExecutionId0',
            description='Description2',
            status=Status1(
                submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                state=CalculationExecutionState1.CANCELING,
                state_change_reason='StateChangeReason8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



