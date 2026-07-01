# Public Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlB1YmxpY05ldA

Public network information

*This model accepts additional fields of type Object.*


# Class Name

`PublicNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `TrueClass \| FalseClass` | Required | Public Interface enabled or not |
| `ipv_4` | [`Ipv4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/ipv-4.md) | Required | IP address (v4) |
| `ipv_6` | [`Ipv6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/ipv-6.md) | Required | IP address (v6) |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
public_net = PublicNet.new(
  enabled: false,
  ipv4: Ipv4.new(
    dns_ptr: 'lb1.example.com',
    ip: '1.2.3.4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  ipv6: Ipv6.new(
    dns_ptr: 'lb1.example.com',
    ip: '2001:db8::1',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



