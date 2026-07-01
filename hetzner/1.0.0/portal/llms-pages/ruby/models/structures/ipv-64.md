# Ipv 64

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRklwdjY0

IPv6 network assigned to this Server and its reverse DNS entry


# Class Name

`Ipv64`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `TrueClass \| FalseClass` | Required | If the IP is blocked by our anti abuse dept |
| `dns_ptr` | [`Array[DnsPtr8]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/dns-ptr-8.md) | Required | Reverse DNS PTR entries for the IPv6 addresses of this Server, `null` by default |
| `id` | `Integer` | Optional | ID of the Resource |
| `ip` | `String` | Required | IP address (v6) of this Server |


# Example

```ruby
ipv64 = Ipv64.new(
  false,
  [
    DnsPtr8.new(
      'server.example.com',
      '2001:db8::1'
    )
  ],
  '2001:db8::/64',
  42
)
```



