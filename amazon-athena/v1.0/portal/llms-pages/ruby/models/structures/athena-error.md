# Athena Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkF0aGVuYUVycm9y

Provides information about an Athena query error. The <code>AthenaError</code> feature provides standardized error information to help you understand failed queries and take steps after a query failure occurs. <code>AthenaError</code> includes an <code>ErrorCategory</code> field that specifies whether the cause of the failed query is due to system error, user error, or other error.


# Class Name

`AthenaError`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error_category` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 3` |
| `error_type` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 9999` |
| `retryable` | `TrueClass \| FalseClass` | Optional | - |
| `error_message` | `String` | Optional | - |


# Example

```ruby
athena_error = AthenaError.new(
  3,
  96,
  false,
  'ErrorMessage0'
)
```



