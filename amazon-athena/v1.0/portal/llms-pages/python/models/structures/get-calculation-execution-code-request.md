# Get Calculation Execution Code Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`GetCalculationExecutionCodeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.get_calculation_execution_code_request import GetCalculationExecutionCodeRequest

get_calculation_execution_code_request = GetCalculationExecutionCodeRequest(
    calculation_execution_id='CalculationExecutionId0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



