# Ipv 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRklwdjY

IP address (v6)


# Class Name

`Ipv6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Optional | Reverse DNS PTR entry for the IPv6 address of this Load Balancer |
| `ip` | `String` | Optional | IP address (v6) of this Load Balancer |


# Example

```ruby
ipv6 = Ipv6.new(
  'lb1.example.com',
  '2001:db8::1'
)
```



