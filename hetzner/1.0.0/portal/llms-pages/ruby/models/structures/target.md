# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlRhcmdldA

*This model accepts additional fields of type Object.*


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `health_status` | [`Array[HealthStatus]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/health-status.md) | Optional | - |
| `server` | [`Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-11.md) | Optional | - |
| `type` | `String` | Optional | - |
| `use_private_ip` | `TrueClass \| FalseClass` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
target = Target.new(
  health_status: [
    HealthStatus.new(
      listen_port: 142,
      status: Status30::UNKNOWN,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    HealthStatus.new(
      listen_port: 142,
      status: Status30::UNKNOWN,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    HealthStatus.new(
      listen_port: 142,
      status: Status30::UNKNOWN,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  server: Server11.new(
    id: 14,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  type: 'server',
  use_private_ip: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



