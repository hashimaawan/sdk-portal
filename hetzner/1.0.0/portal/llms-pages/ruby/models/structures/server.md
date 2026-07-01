# Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcg

*This model accepts additional fields of type Object.*


# Class Name

`Server`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Required | ID of the Resource |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server = Server.new(
  id: 42,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



