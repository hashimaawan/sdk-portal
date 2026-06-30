# Public Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlB1YmxpY05ldDQ

Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip`


# Class Name

`PublicNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewalls` | [`Array[ServerPublicNetFirewall]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/server-public-net-firewall.md) | Optional | Firewalls applied to the public network interface of this Server |
| `floating_ips` | `Array[Integer]` | Required | IDs of Floating IPs assigned to this Server |
| `ipv_4` | [`Ipv44`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/ipv-44.md) | Required | IP address (v4) and its reverse DNS entry of this Server |
| `ipv_6` | [`Ipv64`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/ipv-64.md) | Required | IPv6 network assigned to this Server and its reverse DNS entry |


# Example

```ruby
public_net4 = PublicNet4.new(
  [
    478
  ],
  Ipv44.new(
    false,
    'server01.example.com',
    '1.2.3.4',
    42
  ),
  Ipv64.new(
    false,
    [
      DnsPtr8.new(
        'server.example.com',
        '2001:db8::1'
      )
    ],
    '2001:db8::/64',
    42
  ),
  [
    ServerPublicNetFirewall.new(
      250,
      Status72Enum::APPLIED
    )
  ]
)
```



