# Private Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ0


# Class Name

`PrivateNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alias_ips` | `Array[String]` | Optional | - |
| `ip` | `String` | Optional | - |
| `mac_address` | `String` | Optional | - |
| `network` | `Integer` | Optional | - |


# Example

```ruby
private_net4 = PrivateNet4.new(
  [
    'alias_ips4',
    'alias_ips3'
  ],
  '10.0.0.2',
  '86:00:ff:2a:7d:e1',
  4711
)
```



