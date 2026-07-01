# Public Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlB1YmxpY05ldDQ

Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip`

*This model accepts additional fields of type Object.*


# Class Name

`PublicNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewalls` | [`Array[ServerPublicNetFirewall]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-public-net-firewall.md) | Optional | Firewalls applied to the public network interface of this Server |
| `floating_ips` | `Array[Integer]` | Required | IDs of Floating IPs assigned to this Server |
| `ipv_4` | [`Ipv44`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/ipv-44.md) | Required | IP address (v4) and its reverse DNS entry of this Server |
| `ipv_6` | [`Ipv64`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/ipv-64.md) | Required | IPv6 network assigned to this Server and its reverse DNS entry |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
public_net4 = PublicNet4.new(
  floating_ips: [
    478
  ],
  ipv4: Ipv44.new(
    blocked: false,
    dns_ptr: 'server01.example.com',
    ip: '1.2.3.4',
    id: 42,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  ipv6: Ipv64.new(
    blocked: false,
    dns_ptr: [
      DnsPtr8.new(
        dns_ptr: 'server.example.com',
        ip: '2001:db8::1',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    ip: '2001:db8::/64',
    id: 42,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  firewalls: [
    ServerPublicNetFirewall.new(
      id: 250,
      status: Status72::APPLIED,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



