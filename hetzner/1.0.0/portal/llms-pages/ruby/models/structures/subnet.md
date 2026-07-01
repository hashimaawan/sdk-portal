# Subnet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlN1Ym5ldA

*This model accepts additional fields of type Object.*


# Class Name

`Subnet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gateway` | `String` | Required | Gateway for Servers attached to this subnet. For subnets of type Server this is always the first IP of the network IP range. |
| `ip_range` | `String` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. |
| `network_zone` | `String` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. |
| `type` | [`Type42`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-42.md) | Required | Type of Subnetwork |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
subnet = Subnet.new(
  gateway: '10.0.0.1',
  network_zone: 'eu-central',
  type: Type42::SERVER,
  ip_range: '10.0.1.0/24',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



