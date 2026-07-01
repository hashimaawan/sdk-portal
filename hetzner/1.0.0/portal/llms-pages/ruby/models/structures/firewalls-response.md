# Firewalls Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZpcmV3YWxsc1Jlc3BvbnNl


# Class Name

`FirewallsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewalls` | [`Array[Firewall]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/firewall.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | - |


# Example

```ruby
firewalls_response = FirewallsResponse.new(
  [
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
        'key0': 'labels4',
        'key1': 'labels5'
      }
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



