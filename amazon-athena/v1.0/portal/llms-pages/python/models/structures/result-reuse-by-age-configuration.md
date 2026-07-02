# Result Reuse by Age Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9u

Specifies whether previous query results are reused, and if so, their maximum age.


# Class Name

`ResultReuseByAgeConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `bool` | Required | - |
| `max_age_in_minutes` | `int` | Optional | **Constraints**: `>= 0`, `<= 10080` |


# Example

```python
from amazonathena.models.result_reuse_by_age_configuration import ResultReuseByAgeConfiguration

result_reuse_by_age_configuration = ResultReuseByAgeConfiguration(
    enabled=False,
    max_age_in_minutes=32
)
```



