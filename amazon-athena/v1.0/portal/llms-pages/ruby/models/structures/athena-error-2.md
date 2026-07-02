# Athena Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkF0aGVuYUVycm9yMg


# Class Name

`AthenaError2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error_category` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 3` |
| `error_type` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 9999` |
| `retryable` | `TrueClass \| FalseClass` | Optional | - |
| `error_message` | `String` | Optional | - |


# Example

```ruby
athena_error2 = AthenaError2.new(
  3,
  44,
  false,
  'ErrorMessage4'
)
```



