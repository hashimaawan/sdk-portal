# Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVzcG9uc2U


# Class Name

`FirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/firewall.md) | Required | - |


# Example

```ruby
firewall_response = FirewallResponse.new(
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
)
```



