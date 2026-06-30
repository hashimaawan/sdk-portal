# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkZpcmV3YWxs


# Class Name

`Firewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applied_to` | [`Array[AppliedTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/applied-to.md) | Required | - |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `Integer` | Required | ID of the Resource |
| `labels` | `Hash[String, String]` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the Resource. Must be unique per Project. |
| `rules` | [`Array[Rule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/rule.md) | Required | - |


# Example

```ruby
firewall = Firewall.new(
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
    )
  ],
  '2016-01-30T23:55:00+00:00',
  42,
  'my-resource',
  [
    Rule.new(
      DirectionEnum::ENUM_IN,
      ProtocolEnum::UDP,
      'description2',
      [
        '28.239.13.1/32',
        '28.239.14.0/24',
        'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
      ],
      '80',
      [
        '28.239.13.1/32',
        '28.239.14.0/24',
        'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
      ]
    )
  ],
  {
    'key0': 'labels2',
    'key1': 'labels1'
  }
)
```



