# Get Calculation Execution Code Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`GetCalculationExecutionCodeResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code_block` | `str` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.get_calculation_execution_code_response import GetCalculationExecutionCodeResponse

get_calculation_execution_code_response = GetCalculationExecutionCodeResponse(
    code_block='CodeBlock2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



