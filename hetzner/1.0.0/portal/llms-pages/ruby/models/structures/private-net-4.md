# Private Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ0

*This model accepts additional fields of type Object.*


# Class Name

`PrivateNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alias_ips` | `Array[String]` | Optional | - |
| `ip` | `String` | Optional | - |
| `mac_address` | `String` | Optional | - |
| `network` | `Integer` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
private_net4 = PrivateNet4.new(
  alias_ips: [
    'alias_ips4',
    'alias_ips3'
  ],
  ip: '10.0.0.2',
  mac_address: '86:00:ff:2a:7d:e1',
  network: 4711,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



