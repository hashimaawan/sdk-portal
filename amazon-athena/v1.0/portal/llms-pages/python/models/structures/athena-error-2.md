# Athena Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkF0aGVuYUVycm9yMg


# Class Name

`AthenaError2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error_category` | `int` | Optional | **Constraints**: `>= 1`, `<= 3` |
| `error_type` | `int` | Optional | **Constraints**: `>= 0`, `<= 9999` |
| `retryable` | `bool` | Optional | - |
| `error_message` | `str` | Optional | - |


# Example

```python
from amazonathena.models.athena_error_2 import AthenaError2

athena_error_2 = AthenaError2(
    error_category=3,
    error_type=180,
    retryable=False,
    error_message='ErrorMessage8'
)
```



