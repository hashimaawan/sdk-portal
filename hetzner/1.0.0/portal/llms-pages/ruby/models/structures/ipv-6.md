# Ipv 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRklwdjY

IP address (v6)

*This model accepts additional fields of type Object.*


# Class Name

`Ipv6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Optional | Reverse DNS PTR entry for the IPv6 address of this Load Balancer |
| `ip` | `String` | Optional | IP address (v6) of this Load Balancer |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
ipv6 = Ipv6.new(
  dns_ptr: 'lb1.example.com',
  ip: '2001:db8::1',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



