# Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFjdGlvbnNSZXNwb25zZQ


# Class Name

`ActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`Array[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | - |


# Example

```ruby
actions_response = ActionsResponse.new(
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
  ],
  Meta.new(
    Pagination.new(
      77.7,
      209.18,
      17.58,
      13.34,
      50.02,
      206.64
    )
  )
)
```



