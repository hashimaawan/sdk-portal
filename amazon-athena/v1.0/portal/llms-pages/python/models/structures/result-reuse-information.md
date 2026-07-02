# Result Reuse Information

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24

Contains information about whether the result of a previous query was reused.

*This model accepts additional fields of type Any.*


# Class Name

`ResultReuseInformation`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reused_previous_result` | `bool` | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.result_reuse_information import ResultReuseInformation

result_reuse_information = ResultReuseInformation(
    reused_previous_result=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



