# Actor

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRkFjdG9y

*This model accepts additional fields of type Object.*


# Class Name

`Actor`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account` | `String` | Optional | - |
| `id` | `UUID \| String` | Optional | - |
| `jti` | `String` | Optional | - |
| `request_ip` | `String` | Optional | - |
| `user_agent` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
actor = Actor.new(
  account: 'account0',
  id: '0000193c-0000-0000-0000-000000000000',
  jti: 'jti2',
  request_ip: 'requestIp4',
  user_agent: 'userAgent6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



