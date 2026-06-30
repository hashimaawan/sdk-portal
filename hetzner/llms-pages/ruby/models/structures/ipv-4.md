# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)


# Class Name

`Ipv4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer |
| `ip` | `String` | Optional | IP address (v4) of this Load Balancer |


# Example

```ruby
ipv4 = Ipv4.new(
  'lb1.example.com',
  '1.2.3.4'
)
```



