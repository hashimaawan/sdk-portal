# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `destination_port` | `Integer` | Required | Port the Load Balancer will balance to |
| `health_check` | [`LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/load-balancer-service-health-check.md) | Required | Service health check |
| `http` | [`LoadBalancerServiceHTTP`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https |
| `listen_port` | `Integer` | Required | Port the Load Balancer listens on |
| `protocol` | [`Protocol7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer |
| `proxyprotocol` | `TrueClass \| FalseClass` | Required | Is Proxyprotocol enabled or not |


# Example

```ruby
load_balancer_service = LoadBalancerService.new(
  80,
  LoadBalancerServiceHealthCheck.new(
    15,
    4711,
    Protocol6Enum::HTTP,
    3,
    10,
    Http.new(
      'domain4',
      'path2',
      'response8',
      [
        'status_codes0',
        'status_codes1',
        'status_codes2'
      ],
      false
    )
  ),
  443,
  Protocol7Enum::HTTPS,
  false,
  LoadBalancerServiceHTTP.new(
    [
      180
    ],
    160,
    'cookie_name6',
    false,
    false
  )
)
```



