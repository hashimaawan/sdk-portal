# Server 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcjk

Configuration for type server, required if type is `server`

*This model accepts additional fields of type Object.*


# Class Name

`Server9`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Required | ID of the Server |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server9 = Server9.new(
  id: 216,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



