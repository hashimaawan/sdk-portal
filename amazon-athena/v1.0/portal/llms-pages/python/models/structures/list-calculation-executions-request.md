# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0


# Class Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `state_filter` | [`CalculationExecutionState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/calculation-execution-state-3.md) | Optional | - |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `str` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```python
from amazonathena.models.calculation_execution_state_3_enum import CalculationExecutionState3Enum
from amazonathena.models.list_calculation_executions_request import ListCalculationExecutionsRequest

list_calculation_executions_request = ListCalculationExecutionsRequest(
    session_id='SessionId2',
    state_filter=CalculationExecutionState3Enum.CREATING,
    max_results=100,
    next_token='NextToken0'
)
```



