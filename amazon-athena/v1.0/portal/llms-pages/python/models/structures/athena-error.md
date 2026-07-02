# Athena Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkF0aGVuYUVycm9y

Provides information about an Athena query error. The <code>AthenaError</code> feature provides standardized error information to help you understand failed queries and take steps after a query failure occurs. <code>AthenaError</code> includes an <code>ErrorCategory</code> field that specifies whether the cause of the failed query is due to system error, user error, or other error.


# Class Name

`AthenaError`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error_category` | `int` | Optional | **Constraints**: `>= 1`, `<= 3` |
| `error_type` | `int` | Optional | **Constraints**: `>= 0`, `<= 9999` |
| `retryable` | `bool` | Optional | - |
| `error_message` | `str` | Optional | - |


# Example

```python
from amazonathena.models.athena_error import AthenaError

athena_error = AthenaError(
    error_category=3,
    error_type=96,
    retryable=False,
    error_message='ErrorMessage0'
)
```



