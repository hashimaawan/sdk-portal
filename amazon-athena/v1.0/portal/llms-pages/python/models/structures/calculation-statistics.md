# Calculation Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdGlzdGljcw

Contains statistics for a notebook calculation.

*This model accepts additional fields of type Any.*


# Class Name

`CalculationStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dpu_execution_in_millis` | `int` | Optional | - |
| `progress` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.calculation_statistics import CalculationStatistics

calculation_statistics = CalculationStatistics(
    dpu_execution_in_millis=242,
    progress='Progress6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



