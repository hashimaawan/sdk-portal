# Health Check 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkhlYWx0aENoZWNrMQ

An object specifying health check settings for the load balancer.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`HealthCheck1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `check_interval_seconds` | `Integer` | Optional | The number of seconds between between two consecutive health checks.<br><br>**Default**: `10` |
| `healthy_threshold` | `Integer` | Optional | The number of times a health check must pass for a backend Droplet to be marked "healthy" and be re-added to the pool.<br><br>**Default**: `3` |
| `path` | `String` | Optional | The path on the backend Droplets to which the load balancer instance will send a request.<br><br>**Default**: `'/'` |
| `port` | `Integer` | Optional | An integer representing the port on the backend Droplets on which the health check will attempt a connection.<br><br>**Default**: `80` |
| `protocol` | [`Protocol1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/protocol-1.md) | Optional | The protocol used for health checks sent to the backend Droplets. The possible values are `http`, `https`, or `tcp`.<br><br>**Default**: `Protocol1::HTTP` |
| `response_timeout_seconds` | `Integer` | Optional | The number of seconds the load balancer instance will wait for a response until marking a health check as failed.<br><br>**Default**: `5` |
| `unhealthy_threshold` | `Integer` | Optional | The number of times a health check must fail for a backend Droplet to be marked "unhealthy" and be removed from the pool.<br><br>**Default**: `5` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
health_check1 = HealthCheck1.new(
  check_interval_seconds: 10,
  healthy_threshold: 3,
  path: '/',
  port: 80,
  protocol: Protocol1::HTTP,
  response_timeout_seconds: 5,
  unhealthy_threshold: 5,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



