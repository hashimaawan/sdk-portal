# Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkVycm9yMg

If issuance or renewal reports `failed`, this property contains information about what happened

*This model accepts additional fields of type Object.*


# Class Name

`Error2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `String` | Optional | - |
| `message` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
error2 = Error2.new(
  code: 'code2',
  message: 'message4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



