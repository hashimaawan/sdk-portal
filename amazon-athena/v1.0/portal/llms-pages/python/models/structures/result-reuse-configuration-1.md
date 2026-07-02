# Result Reuse Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbjE

*This model accepts additional fields of type Any.*


# Class Name

`ResultReuseConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `result_reuse_by_age_configuration` | [`ResultReuseByAgeConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.result_reuse_by_age_configuration_2 import ResultReuseByAgeConfiguration2
from amazonathena.models.result_reuse_configuration_1 import ResultReuseConfiguration1

result_reuse_configuration_1 = ResultReuseConfiguration1(
    result_reuse_by_age_configuration=ResultReuseByAgeConfiguration2(
        enabled=False,
        max_age_in_minutes=26,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



