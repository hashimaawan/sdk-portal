# Add Delete Route Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFkZERlbGV0ZVJvdXRlUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`AddDeleteRouteRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `destination` | `String` | Required | Destination network or host of this route. Must not overlap with an existing ip_range in any subnets or with any destinations in other routes or with the first IP of the networks ip_range or with 172.31.1.1. Must be one of the private IPv4 ranges of RFC1918. |
| `gateway` | `String` | Required | Gateway for the route. Cannot be the first IP of the networks ip_range, an IP behind a vSwitch or 172.31.1.1, as this IP is being used as a gateway for the public network interface of Servers. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
add_delete_route_request = AddDeleteRouteRequest.new(
  destination: '10.100.1.0/24',
  gateway: '10.0.1.1',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



