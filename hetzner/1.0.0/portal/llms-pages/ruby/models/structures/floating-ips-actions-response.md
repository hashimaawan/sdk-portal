# Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMEFjdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`Array[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
floating_ips_actions_response = FloatingIpsActionsResponse.new(
  actions: [
    Action.new(
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
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



