# Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMEFjdGlvbnMlMjUyMFJlc3BvbnNl


# Class Name

`FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`Array[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action.md) | Required | - |


# Example

```ruby
floating_ips_actions_response = FloatingIpsActionsResponse.new(
  [
    Action.new(
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
  ]
)
```



