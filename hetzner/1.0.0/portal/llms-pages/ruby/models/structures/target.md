# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlRhcmdldA


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `health_status` | [`Array[HealthStatus]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/health-status.md) | Optional | - |
| `server` | [`Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-11.md) | Optional | - |
| `type` | `String` | Optional | - |
| `use_private_ip` | `TrueClass \| FalseClass` | Optional | - |


# Example

```ruby
target = Target.new(
  [
    HealthStatus.new(
      142,
      Status30Enum::UNKNOWN
    ),
    HealthStatus.new(
      142,
      Status30Enum::UNKNOWN
    ),
    HealthStatus.new(
      142,
      Status30Enum::UNKNOWN
    )
  ],
  Server11.new(
    14
  ),
  'server',
  false
)
```



