# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkVycm9y

Error message for the Action if error occurred, otherwise null

*This model accepts additional fields of type Object.*


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `String` | Required | Fixed machine readable code |
| `message` | `String` | Required | Humanized error message |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
error = Error.new(
  code: 'action_failed',
  message: 'Action failed',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



