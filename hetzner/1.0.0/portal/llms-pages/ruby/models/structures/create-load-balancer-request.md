# Create Load Balancer Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUxvYWRCYWxhbmNlclJlcXVlc3Q


# Class Name

`CreateLoadBalancerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `algorithm` | [`LoadBalancerAlgorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-algorithm.md) | Required | Algorithm of the Load Balancer |
| `labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `load_balancer_type` | `String` | Required | ID or name of the Load Balancer type this Load Balancer should be created with |
| `location` | `String` | Optional | ID or name of Location to create Load Balancer in |
| `name` | `String` | Required | Name of the Load Balancer |
| `network` | `Integer` | Optional | ID of the network the Load Balancer should be attached to on creation |
| `network_zone` | `String` | Optional | Name of network zone |
| `public_interface` | `TrueClass \| FalseClass` | Optional | Enable or disable the public interface of the Load Balancer |
| `services` | [`Array[LoadBalancerService]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-service.md) | Optional | Array of services |
| `targets` | [`Array[LoadBalancerTarget]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-target.md) | Optional | Array of targets |


# Example

```ruby
create_load_balancer_request = CreateLoadBalancerRequest.new(
  LoadBalancerAlgorithm.new(
    Type28Enum::ROUND_ROBIN
  ),
  'lb11',
  'Web Frontend',
  Labels.new(
    'labelkey4'
  ),
  'location8',
  123,
  'eu-central',
  true,
  [],
  []
)
```



