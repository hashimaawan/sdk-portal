# Session Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0aXN0aWNz

Contains statistics for a session.

*This model accepts additional fields of type Any.*


# Class Name

`SessionStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dpu_execution_in_millis` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.session_statistics import SessionStatistics

session_statistics = SessionStatistics(
    dpu_execution_in_millis=136,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



