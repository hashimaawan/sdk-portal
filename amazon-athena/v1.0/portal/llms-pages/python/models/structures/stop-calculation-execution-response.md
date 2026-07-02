# Stop Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlc3BvbnNl


# Class Name

`StopCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`CalculationExecutionState4Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/calculation-execution-state-4.md) | Optional | - |


# Example

```python
from amazonathena.models.calculation_execution_state_4_enum import CalculationExecutionState4Enum
from amazonathena.models.stop_calculation_execution_response import StopCalculationExecutionResponse

stop_calculation_execution_response = StopCalculationExecutionResponse(
    state=CalculationExecutionState4Enum.QUEUED
)
```



