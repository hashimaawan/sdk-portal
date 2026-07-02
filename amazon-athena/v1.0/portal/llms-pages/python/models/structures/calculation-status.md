# Calculation Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdHVz

Contains information about the status of a notebook calculation.


# Class Name

`CalculationStatus`


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
from amazonathena.models.calculation_status import CalculationStatus

calculation_status = CalculationStatus(
    submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    state=CalculationExecutionState1Enum.CREATING,
    state_change_reason='StateChangeReason4'
)
```



