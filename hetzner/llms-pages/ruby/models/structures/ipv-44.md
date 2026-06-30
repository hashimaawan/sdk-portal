# Ipv 44

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRklwdjQ0

IP address (v4) and its reverse DNS entry of this Server


# Class Name

`Ipv44`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `TrueClass \| FalseClass` | Required | If the IP is blocked by our anti abuse dept |
| `dns_ptr` | `String` | Required | Reverse DNS PTR entry for the IPv4 addresses of this Server |
| `id` | `Integer` | Optional | ID of the Resource |
| `ip` | `String` | Required | IP address (v4) of this Server |


# Example

```ruby
ipv44 = Ipv44.new(
  false,
  'server01.example.com',
  '1.2.3.4',
  42
)
```



