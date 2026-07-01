# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `listen_port` | `Integer` | Optional | - |
| `status` | [`Status30Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/status-30.md) | Optional | - |


# Example

```ruby
health_status = HealthStatus.new(
  443,
  Status30Enum::HEALTHY
)
```



