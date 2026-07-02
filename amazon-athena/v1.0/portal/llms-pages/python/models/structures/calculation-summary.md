# Calculation Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3VtbWFyeQ

Summary information for a notebook calculation.


# Class Name

`CalculationSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/status-1.md) | Optional | - |


# Example

```python
import dateutil.parser

from amazonathena.models.calculation_execution_state_1_enum import CalculationExecutionState1Enum
from amazonathena.models.calculation_summary import CalculationSummary
from amazonathena.models.status_1 import Status1

calculation_summary = CalculationSummary(
    calculation_execution_id='CalculationExecutionId2',
    description='Description4',
    status=Status1(
        submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        state=CalculationExecutionState1Enum.CANCELING,
        state_change_reason='StateChangeReason8'
    )
)
```



