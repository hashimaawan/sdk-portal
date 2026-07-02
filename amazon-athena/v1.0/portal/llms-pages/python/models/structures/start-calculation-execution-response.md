# Start Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXNwb25zZQ

*This model accepts additional fields of type Any.*


# Class Name

`StartCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `state` | [`CalculationExecutionState4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/calculation-execution-state-4.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.calculation_execution_state_4 import CalculationExecutionState4
from amazonathena.models.start_calculation_execution_response import StartCalculationExecutionResponse

start_calculation_execution_response = StartCalculationExecutionResponse(
    calculation_execution_id='CalculationExecutionId0',
    state=CalculationExecutionState4.CANCELING,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



