# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.

*This model accepts additional fields of type Any.*


# Class Name

`CalculationConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code_block` | `str` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.calculation_configuration import CalculationConfiguration

calculation_configuration = CalculationConfiguration(
    code_block='CodeBlock6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



