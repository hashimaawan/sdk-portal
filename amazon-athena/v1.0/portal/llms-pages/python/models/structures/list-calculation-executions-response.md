# List Calculation Executions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXNwb25zZQ


# Class Name

`ListCalculationExecutionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `str` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `calculations` | [`List[CalculationSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/calculation-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |


# Example

```python
import dateutil.parser

from amazonathena.models.calculation_execution_state_1_enum import CalculationExecutionState1Enum
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
                state=CalculationExecutionState1Enum.CANCELING,
                state_change_reason='StateChangeReason8'
            )
        ),
        CalculationSummary(
            calculation_execution_id='CalculationExecutionId0',
            description='Description2',
            status=Status1(
                submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                state=CalculationExecutionState1Enum.CANCELING,
                state_change_reason='StateChangeReason8'
            )
        )
    ]
)
```



