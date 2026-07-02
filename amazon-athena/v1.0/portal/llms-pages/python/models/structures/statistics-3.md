# Statistics 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mz

*This model accepts additional fields of type Any.*


# Class Name

`Statistics3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dpu_execution_in_millis` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.statistics_3 import Statistics3

statistics_3 = Statistics3(
    dpu_execution_in_millis=122,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



