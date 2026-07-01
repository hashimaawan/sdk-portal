# Load Balancer Service Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIZWFsdGhDaGVjaw

Service health check


# Class Name

`LoadBalancerServiceHealthCheck`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `http` | [`Http`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/http.md) | Optional | Additional configuration for protocol http |
| `interval` | `Integer` | Required | Time interval in seconds health checks are performed |
| `port` | `Integer` | Required | Port the health check will be performed on |
| `protocol` | [`Protocol6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/protocol-6.md) | Required | Type of the health check |
| `retries` | `Integer` | Required | Unsuccessful retries needed until a target is considered unhealthy; an unhealthy target needs the same number of successful retries to become healthy again |
| `timeout` | `Integer` | Required | Time in seconds after an attempt is considered a timeout |


# Example

```ruby
load_balancer_service_health_check = LoadBalancerServiceHealthCheck.new(
  interval: 15,
  port: 4711,
  protocol: Protocol6::HTTP,
  retries: 3,
  timeout: 10,
  http: Http.new(
    domain: 'domain4',
    path: 'path2',
    response: 'response8',
    status_codes: [
      'status_codes0',
      'status_codes1',
      'status_codes2'
    ],
    tls: false
  )
)
```



