# Public Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlB1YmxpY05ldA

Public network information


# Class Name

`PublicNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `TrueClass \| FalseClass` | Required | Public Interface enabled or not |
| `ipv_4` | [`Ipv4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/ipv-4.md) | Required | IP address (v4) |
| `ipv_6` | [`Ipv6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/ipv-6.md) | Required | IP address (v6) |


# Example

```ruby
public_net = PublicNet.new(
  false,
  Ipv4.new(
    'lb1.example.com',
    '1.2.3.4'
  ),
  Ipv6.new(
    'lb1.example.com',
    '2001:db8::1'
  )
)
```



