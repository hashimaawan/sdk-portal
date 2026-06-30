# Create Server Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlc3BvbnNl


# Class Name

`CreateServerResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/action.md) | Required | - |
| `next_actions` | [`Array[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/action.md) | Required | - |
| `root_password` | `String` | Required | Root password when no SSH keys have been specified |
| `server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/server-18.md) | Required | - |


# Example

```ruby
create_server_response = CreateServerResponse.new(
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
  ),
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
  'YItygq1v3GYjjMomLaKc',
  Server18.new(
    '22-02',
    '2016-01-30T23:55:00+00:00',
    Datacenter6.new(
      'Falkenstein DC Park 8',
      42,
      Location.new(
        'Falkenstein',
        'DE',
        'Falkenstein DC Park 1',
        1,
        50.47612,
        12.370071,
        'fsn1',
        'eu-central'
      ),
      'fsn1-dc8',
      ServerTypes.new(
        [
          1,
          2,
          3
        ],
        [
          1,
          2,
          3
        ],
        [
          1,
          2,
          3
        ]
      )
    ),
    42,
    Image.new(
      nil,
      '2016-01-30T23:55:00+00:00',
      CreatedFrom.new(
        1,
        'Server'
      ),
      nil,
      '2018-02-28T00:00:00+00:00',
      'Ubuntu 20.04 Standard 64 bit',
      10,
      42,
      2.3,
      {
        'key0': 'labels4'
      },
      'ubuntu-20.04',
      OsFlavorEnum::UBUNTU,
      '20.04',
      Protection.new(
        false
      ),
      Status24Enum::UNAVAILABLE,
      Type22Enum::SNAPSHOT,
      false
    ),
    654321,
    123456,
    Iso2.new(
      '2018-02-28T00:00:00+00:00',
      'FreeBSD 11.0 x64',
      42,
      'FreeBSD-11.0-RELEASE-amd64-dvd1',
      Type26Enum::PUBLIC
    ),
    {
      'key0': 'labels0',
      'key1': 'labels9'
    },
    false,
    'my-resource',
    123456,
    50,
    [
      PrivateNet4.new(
        [
          'alias_ips4'
        ],
        '10.0.0.2',
        '86:00:ff:2a:7d:e1',
        4711
      )
    ],
    Protection20.new(
      false,
      false
    ),
    PublicNet4.new(
      [
        478
      ],
      Ipv44.new(
        false,
        'server01.example.com',
        '1.2.3.4',
        42
      ),
      Ipv64.new(
        false,
        [
          DnsPtr8.new(
            'server.example.com',
            '2001:db8::1'
          )
        ],
        '2001:db8::/64',
        42
      ),
      [
        ServerPublicNetFirewall.new(
          250,
          Status72Enum::APPLIED
        ),
        ServerPublicNetFirewall.new(
          250,
          Status72Enum::APPLIED
        )
      ]
    ),
    false,
    ServerType1.new(
      1,
      CpuTypeEnum::SHARED,
      false,
      'CX11',
      25,
      1,
      1,
      'cx11',
      [
        Price9.new(
          'fsn1',
          PriceHourly8.new(
            '1.1900000000000000',
            '1.0000000000'
          ),
          PriceMonthly10.new(
            '1.1900000000000000',
            '1.0000000000'
          )
        )
      ],
      StorageTypeEnum::LOCAL
    ),
    Status73Enum::STARTING,
    [
      144,
      143,
      142
    ],
    PlacementGroupNullable.new(
      'created8',
      236,
      {
        'key0': 'labels4'
      },
      'name8',
      [
        251,
        252,
        253
      ],
      'type2'
    ),
    [
      91,
      92
    ]
  )
)
```



