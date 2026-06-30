# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA


# Class Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apply_to` | [`Array[ApplyTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the Firewall |
| `rules` | [`Array[Rule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/rule.md) | Optional | Array of rules |


# Example

```ruby
create_firewall_request = CreateFirewallRequest.new(
  'Corporate Intranet Protection',
  [
    ApplyTo.new(
      Type7Enum::SERVER,
      LabelSelector1.new(
        'selector8'
      ),
      Server2.new(
        14
      )
    ),
    ApplyTo.new(
      Type7Enum::SERVER,
      LabelSelector1.new(
        'selector8'
      ),
      Server2.new(
        14
      )
    ),
    ApplyTo.new(
      Type7Enum::SERVER,
      LabelSelector1.new(
        'selector8'
      ),
      Server2.new(
        14
      )
    )
  ],
  { 'key1' => 'val1', 'key2' => 'val2' },
  [
    Rule.new(
      DirectionEnum::ENUM_IN,
      ProtocolEnum::TCP,
      'description2',
      [
        'destination_ips1',
        'destination_ips2',
        'destination_ips3'
      ],
      '80',
      [
        '28.239.13.1/32',
        '28.239.14.0/24',
        'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
      ]
    )
  ]
)
```



