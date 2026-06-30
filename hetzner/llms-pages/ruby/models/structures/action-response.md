# Action Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkFjdGlvblJlc3BvbnNl


# Class Name

`ActionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/action.md) | Required | - |


# Example

```ruby
action_response = ActionResponse.new(
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
    StatusEnum::RUNNING
  )
)
```



