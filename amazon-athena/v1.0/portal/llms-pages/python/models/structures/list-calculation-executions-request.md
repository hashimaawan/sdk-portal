# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `state_filter` | [`CalculationExecutionState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/calculation-execution-state-3.md) | Optional | - |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `str` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.calculation_execution_state_3 import CalculationExecutionState3
from amazonathena.models.list_calculation_executions_request import ListCalculationExecutionsRequest

list_calculation_executions_request = ListCalculationExecutionsRequest(
    session_id='SessionId2',
    state_filter=CalculationExecutionState3.CREATING,
    max_results=100,
    next_token='NextToken0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



