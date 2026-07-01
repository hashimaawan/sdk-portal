# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ

*This model accepts additional fields of type Object.*


# Class Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | `String` | Optional | - |
| `network` | `Integer` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
private_net = PrivateNet.new(
  ip: '10.0.0.2',
  network: 4711,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



