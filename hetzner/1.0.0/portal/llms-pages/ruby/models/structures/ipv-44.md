# Ipv 44

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRklwdjQ0

IP address (v4) and its reverse DNS entry of this Server

*This model accepts additional fields of type Object.*


# Class Name

`Ipv44`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `TrueClass \| FalseClass` | Required | If the IP is blocked by our anti abuse dept |
| `dns_ptr` | `String` | Required | Reverse DNS PTR entry for the IPv4 addresses of this Server |
| `id` | `Integer` | Optional | ID of the Resource |
| `ip` | `String` | Required | IP address (v4) of this Server |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
ipv44 = Ipv44.new(
  blocked: false,
  dns_ptr: 'server01.example.com',
  ip: '1.2.3.4',
  id: 42,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



