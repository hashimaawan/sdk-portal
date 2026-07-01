# Server 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcjEx

*This model accepts additional fields of type Object.*


# Class Name

`Server11`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Required | ID of the Server |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server11 = Server11.new(
  id: 85,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



