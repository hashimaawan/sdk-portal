# Status 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXR1czE


# Class Name

`Status1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `submission_date_time` | `datetime` | Optional | - |
| `completion_date_time` | `datetime` | Optional | - |
| `state` | [`CalculationExecutionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/calculation-execution-state-1.md) | Optional | - |
| `state_change_reason` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```python
import dateutil.parser

from amazonathena.models.calculation_execution_state_1_enum import CalculationExecutionState1Enum
from amazonathena.models.status_1 import Status1

status_1 = Status1(
    submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    state=CalculationExecutionState1Enum.COMPLETED,
    state_change_reason='StateChangeReason4'
)
```



