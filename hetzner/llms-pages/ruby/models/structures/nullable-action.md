# Nullable Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRk51bGxhYmxlQWN0aW9u


# Class Name

`NullableAction`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `command` | `String` | Required | Command executed in the Action |
| `error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/error.md) | Required | Error message for the Action if error occurred, otherwise null |
| `finished` | `String` | Required | Point in time when the Action was finished (in ISO-8601 format). Only set if the Action is finished otherwise null. |
| `id` | `Integer` | Required | ID of the Resource |
| `progress` | `Float` | Required | Progress of Action in percent |
| `resources` | [`Array[Resource]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/resource.md) | Required | Resources the Action relates to |
| `started` | `String` | Required | Point in time when the Action was started (in ISO-8601 format) |
| `status` | [`StatusEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/status.md) | Required | Status of the Action |


# Example

```ruby
nullable_action = NullableAction.new(
  'start_server',
  Error.new(
    'action_failed',
    'Action failed'
  ),
  '2016-01-30T23:55:00+00:00',
  42,
  100,
  [
    Resource.new(
      42,
      'server'
    )
  ],
  '2016-01-30T23:55:00+00:00',
  StatusEnum::SUCCESS
)
```



