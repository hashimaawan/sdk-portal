# Create Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZU5ldHdvcmtSZXF1ZXN0


# Class Name

`CreateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip_range` | `String` | Required | IP range of the whole network which must span all included subnets. Must be one of the private IPv4 ranges of RFC1918. Minimum network size is /24. We highly recommend that you pick a larger network with a /16 netmask. |
| `labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the network |
| `routes` | [`Array[Route]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/route.md) | Optional | Array of routes set in this network. The destination of the route must be one of the private IPv4 ranges of RFC1918. The gateway must be a subnet/IP of the ip_range of the network object. The destination must not overlap with an existing ip_range in any subnets or with any destinations in other routes or with the first IP of the networks ip_range or with 172.31.1.1. The gateway cannot be the first IP of the networks ip_range and also cannot be 172.31.1.1. |
| `subnets` | [`Array[Subnet1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/subnet-1.md) | Optional | Array of subnets allocated. |


# Example

```ruby
create_network_request = CreateNetworkRequest.new(
  '10.0.0.0/16',
  'mynet',
  Labels.new(
    'labelkey4'
  ),
  [
    Route.new(
      'destination8',
      'gateway6'
    ),
    Route.new(
      'destination8',
      'gateway6'
    ),
    Route.new(
      'destination8',
      'gateway6'
    )
  ],
  [
    Subnet1.new(
      'network_zone2',
      Type42Enum::CLOUD,
      'ip_range6'
    )
  ]
)
```



