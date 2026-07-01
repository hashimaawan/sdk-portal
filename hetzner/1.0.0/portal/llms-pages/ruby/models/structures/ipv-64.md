# Ipv 64

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRklwdjY0

IPv6 network assigned to this Server and its reverse DNS entry

*This model accepts additional fields of type Object.*


# Class Name

`Ipv64`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `TrueClass \| FalseClass` | Required | If the IP is blocked by our anti abuse dept |
| `dns_ptr` | [`Array[DnsPtr8]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/dns-ptr-8.md) | Required | Reverse DNS PTR entries for the IPv6 addresses of this Server, `null` by default |
| `id` | `Integer` | Optional | ID of the Resource |
| `ip` | `String` | Required | IP address (v6) of this Server |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
ipv64 = Ipv64.new(
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
)
```



