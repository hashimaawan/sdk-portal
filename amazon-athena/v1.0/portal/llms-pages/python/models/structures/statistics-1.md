# Statistics 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mx

*This model accepts additional fields of type Any.*


# Class Name

`Statistics1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dpu_execution_in_millis` | `int` | Optional | - |
| `progress` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.statistics_1 import Statistics1

statistics_1 = Statistics1(
    dpu_execution_in_millis=138,
    progress='Progress4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



