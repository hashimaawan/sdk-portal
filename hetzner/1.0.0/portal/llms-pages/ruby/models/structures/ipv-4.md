# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)

*This model accepts additional fields of type Object.*


# Class Name

`Ipv4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer |
| `ip` | `String` | Optional | IP address (v4) of this Load Balancer |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
ipv4 = Ipv4.new(
  dns_ptr: 'lb1.example.com',
  ip: '1.2.3.4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



