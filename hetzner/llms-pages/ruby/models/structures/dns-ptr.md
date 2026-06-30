# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkRuc1B0cg


# Class Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Required | DNS pointer for the specific IP address |
| `ip` | `String` | Required | Single IPv4 or IPv6 address |


# Example

```ruby
dns_ptr = DnsPtr.new(
  'server.example.com',
  '2001:db8::1'
)
```



