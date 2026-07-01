# Nullable Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRk51bGxhYmxlQWN0aW9u

*This model accepts additional fields of type Object.*


# Class Name

`NullableAction`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `command` | `String` | Required | Command executed in the Action |
| `error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/error.md) | Required | Error message for the Action if error occurred, otherwise null |
| `finished` | `String` | Required | Point in time when the Action was finished (in ISO-8601 format). Only set if the Action is finished otherwise null. |
| `id` | `Integer` | Required | ID of the Resource |
| `progress` | `Float` | Required | Progress of Action in percent |
| `resources` | [`Array[Resource]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/resource.md) | Required | Resources the Action relates to |
| `started` | `String` | Required | Point in time when the Action was started (in ISO-8601 format) |
| `status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/status.md) | Required | Status of the Action |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
nullable_action = NullableAction.new(
  command: 'start_server',
  error: Error.new(
    code: 'action_failed',
    message: 'Action failed',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  finished: '2016-01-30T23:55:00+00:00',
  id: 42,
  progress: 100,
  resources: [
    Resource.new(
      id: 42,
      type: 'server',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  started: '2016-01-30T23:55:00+00:00',
  status: Status::SUCCESS,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



