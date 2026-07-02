# Sticky Sessions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0aWNreVNlc3Npb25z

An object specifying sticky sessions settings for the load balancer.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`StickySessions`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cookie_name` | `String` | Optional | The name of the cookie sent to the client. This attribute is only returned when using `cookies` for the sticky sessions type. |
| `cookie_ttl_seconds` | `Integer` | Optional | The number of seconds until the cookie set by the load balancer expires. This attribute is only returned when using `cookies` for the sticky sessions type. |
| `type` | [`Type16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/type-16.md) | Optional | An attribute indicating how and if requests from a client will be persistently served by the same backend Droplet. The possible values are `cookies` or `none`.<br><br>**Default**: `Type16::NONE` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
sticky_sessions = StickySessions.new(
  cookie_name: 'DO-LB',
  cookie_ttl_seconds: 300,
  type: Type16::COOKIES,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



