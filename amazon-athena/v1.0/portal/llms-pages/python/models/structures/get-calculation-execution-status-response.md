# Get Calculation Execution Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVzcG9uc2U


# Class Name

`GetCalculationExecutionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/status-1.md) | Optional | - |
| `statistics` | [`Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/statistics-1.md) | Optional | - |


# Example

```python
import dateutil.parser

from amazonathena.models.calculation_execution_state_1_enum import CalculationExecutionState1Enum
from amazonathena.models.get_calculation_execution_status_response import GetCalculationExecutionStatusResponse
from amazonathena.models.statistics_1 import Statistics1
from amazonathena.models.status_1 import Status1

get_calculation_execution_status_response = GetCalculationExecutionStatusResponse(
    status=Status1(
        submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        state=CalculationExecutionState1Enum.CANCELING,
        state_change_reason='StateChangeReason8'
    ),
    statistics=Statistics1(
        dpu_execution_in_millis=164,
        progress='Progress6'
    )
)
```



