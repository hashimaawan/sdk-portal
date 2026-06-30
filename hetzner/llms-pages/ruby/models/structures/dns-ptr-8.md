# Dns Ptr 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkRuc1B0cjg


# Class Name

`DnsPtr8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Required | DNS pointer for the specific IP address |
| `ip` | `String` | Required | Single IPv6 address of this Server for which the reverse DNS entry has been set up |


# Example

```ruby
dns_ptr8 = DnsPtr8.new(
  'server.example.com',
  '2001:db8::1'
)
```



