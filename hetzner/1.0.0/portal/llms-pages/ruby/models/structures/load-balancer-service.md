# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `destination_port` | `Integer` | Required | Port the Load Balancer will balance to |
| `health_check` | [`LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-service-health-check.md) | Required | Service health check |
| `http` | [`LoadBalancerServiceHttp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https |
| `listen_port` | `Integer` | Required | Port the Load Balancer listens on |
| `protocol` | [`Protocol7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer |
| `proxyprotocol` | `TrueClass \| FalseClass` | Required | Is Proxyprotocol enabled or not |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancer_service = LoadBalancerService.new(
  destination_port: 80,
  health_check: LoadBalancerServiceHealthCheck.new(
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
  ),
  listen_port: 443,
  protocol: Protocol7::HTTPS,
  proxyprotocol: false,
  http: LoadBalancerServiceHttp.new(
    certificates: [
      180
    ],
    cookie_lifetime: 160,
    cookie_name: 'cookie_name6',
    redirect_http: false,
    sticky_sessions: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



