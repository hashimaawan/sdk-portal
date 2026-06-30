# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`Array[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/action.md) | Optional | - |
| `firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/firewall.md) | Optional | - |


# Example

```ruby
create_firewall_response = CreateFirewallResponse.new(
  [
    Action.new(
      'set_firewall_rules',
      Error.new(
        'action_failed',
        'Action failed'
      ),
      '2016-01-30T23:56:00+00:00',
      13,
      100,
      [
        Resource.new(
          38,
          'firewall'
        )
      ],
      '2016-01-30T23:55:00+00:00',
      StatusEnum::SUCCESS
    ),
    Action.new(
      'apply_firewall',
      Error.new(
        'action_failed',
        'Action failed'
      ),
      '2016-01-30T23:56:00+00:00',
      14,
      100,
      [
        Resource.new(
          42,
          'server'
        ),
        Resource.new(
          38,
          'firewall'
        )
      ],
      '2016-01-30T23:55:00+00:00',
      StatusEnum::SUCCESS
    )
  ],
  Firewall.new(
    [
      AppliedTo.new(
        Type6Enum::SERVER,
        [
          AppliedToResource.new(
            Server.new(
              14
            ),
            Type5Enum::SERVER
          )
        ],
        LabelSelector.new(
          'selector8'
        ),
        Server.new(
          14
        )
      ),
      AppliedTo.new(
        Type6Enum::SERVER,
        [
          AppliedToResource.new(
            Server.new(
              14
            ),
            Type5Enum::SERVER
          )
        ],
        LabelSelector.new(
          'selector8'
        ),
        Server.new(
          14
        )
      )
    ],
    'created6',
    4,
    'name6',
    [
      Rule.new(
        DirectionEnum::ENUM_IN,
        ProtocolEnum::UDP,
        'description2',
        [
          'destination_ips1',
          'destination_ips2',
          'destination_ips3'
        ],
        'port8',
        [
          'source_ips1',
          'source_ips2',
          'source_ips3'
        ]
      )
    ],
    {
      'key0': 'labels2',
      'key1': 'labels1'
    }
  )
)
```



