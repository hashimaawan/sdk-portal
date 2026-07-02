# Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkhlYWx0aENoZWNr

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`HealthCheck`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `failure_threshold` | `Integer` | Optional | The number of failed health checks before considered unhealthy. |
| `http_path` | `String` | Optional | The route path used for the HTTP health check ping. If not set, the HTTP health check will be disabled and a TCP health check used instead. |
| `initial_delay_seconds` | `Integer` | Optional | The number of seconds to wait before beginning health checks. |
| `period_seconds` | `Integer` | Optional | The number of seconds to wait between health checks. |
| `port` | `Integer` | Optional | The port on which the health check will be performed. If not set, the health check will be performed on the component's http_port.<br><br>**Constraints**: `>= 1`, `<= 65535` |
| `success_threshold` | `Integer` | Optional | The number of successful health checks before considered healthy. |
| `timeout_seconds` | `Integer` | Optional | The number of seconds after which the check times out. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
health_check = HealthCheck.new(
  failure_threshold: 2,
  http_path: '/health',
  initial_delay_seconds: 30,
  period_seconds: 60,
  port: 80,
  success_threshold: 3,
  timeout_seconds: 45,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



