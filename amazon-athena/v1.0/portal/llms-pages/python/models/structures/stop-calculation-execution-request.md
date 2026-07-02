# Stop Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`StopCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.stop_calculation_execution_request import StopCalculationExecutionRequest

stop_calculation_execution_request = StopCalculationExecutionRequest(
    calculation_execution_id='CalculationExecutionId2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



