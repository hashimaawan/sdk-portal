# Result Reuse by Age Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9u

Specifies whether previous query results are reused, and if so, their maximum age.

*This model accepts additional fields of type Any.*


# Class Name

`ResultReuseByAgeConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `bool` | Required | - |
| `max_age_in_minutes` | `int` | Optional | **Constraints**: `>= 0`, `<= 10080` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.result_reuse_by_age_configuration import ResultReuseByAgeConfiguration

result_reuse_by_age_configuration = ResultReuseByAgeConfiguration(
    enabled=False,
    max_age_in_minutes=32,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



