# Public Net 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlB1YmxpY05ldDU

Public Network options


# Class Name

`PublicNet5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enable_ipv_4` | `TrueClass \| FalseClass` | Optional | Attach an IPv4 on the public NIC. If false, no IPv4 address will be attached. Defaults to true. |
| `enable_ipv_6` | `TrueClass \| FalseClass` | Optional | Attach an IPv6 on the public NIC. If false, no IPv6 address will be attached. Defaults to true. |
| `ipv_4` | `Integer` | Optional | ID of the ipv4 Primary IP to use. If omitted and enable_ipv4 is true, a new ipv4 Primary IP will automatically be created. |
| `ipv_6` | `Integer` | Optional | ID of the ipv6 Primary IP to use. If omitted and enable_ipv6 is true, a new ipv6 Primary IP will automatically be created. |


# Example

```ruby
public_net5 = PublicNet5.new(
  false,
  false,
  58,
  86
)
```



