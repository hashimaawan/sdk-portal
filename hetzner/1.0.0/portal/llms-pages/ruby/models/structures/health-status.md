# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw

*This model accepts additional fields of type Object.*


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `listen_port` | `Integer` | Optional | - |
| `status` | [`Status30`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/status-30.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
health_status = HealthStatus.new(
  listen_port: 443,
  status: Status30::HEALTHY,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



