# Server 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcjI

Configuration for type Server, required if type is `server`

*This model accepts additional fields of type Object.*


# Class Name

`Server2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Required | ID of the Server |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server2 = Server2.new(
  id: 162,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



