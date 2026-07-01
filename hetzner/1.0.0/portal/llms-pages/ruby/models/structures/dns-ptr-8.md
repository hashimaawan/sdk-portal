# Dns Ptr 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkRuc1B0cjg

*This model accepts additional fields of type Object.*


# Class Name

`DnsPtr8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Required | DNS pointer for the specific IP address |
| `ip` | `String` | Required | Single IPv6 address of this Server for which the reverse DNS entry has been set up |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
dns_ptr8 = DnsPtr8.new(
  dns_ptr: 'server.example.com',
  ip: '2001:db8::1',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



