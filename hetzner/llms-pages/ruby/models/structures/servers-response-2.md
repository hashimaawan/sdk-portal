# Servers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMg


# Class Name

`ServersResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/server-18.md) | Optional | - |


# Example

```ruby
servers_response2 = ServersResponse2.new(
  Server18.new(
    'backup_window2',
    'created4',
    Datacenter6.new(
      'description0',
      200,
      Location.new(
        'city6',
        'country8',
        'description6',
        187.14,
        194.62,
        59.18,
        'name4',
        'network_zone2'
      ),
      'name0',
      ServerTypes.new(
        [
          23.74
        ],
        [
          201.65,
          201.66
        ],
        [
          69.52,
          69.53,
          69.54
        ]
      )
    ),
    14,
    Image.new(
      186,
      'created6',
      CreatedFrom.new(
        60,
        'name6'
      ),
      'deleted4',
      'deprecated8',
      'description6',
      244.18,
      128,
      141.34,
      {
        'key0': 'labels4'
      },
      'name6',
      OsFlavorEnum::DEBIAN,
      'os_version4',
      Protection.new(
        false
      ),
      Status24Enum::UNAVAILABLE,
      Type22Enum::APP,
      false
    ),
    123.68,
    151.82,
    Iso2.new(
      'deprecated0',
      'description2',
      66,
      'name8',
      Type26Enum::PUBLIC
    ),
    {
      'key0': 'labels0',
      'key1': 'labels9'
    },
    false,
    'name4',
    129.6,
    19.88,
    [
      PrivateNet4.new(
        [
          'alias_ips4'
        ],
        'ip6',
        'mac_address0',
        154
      ),
      PrivateNet4.new(
        [
          'alias_ips4'
        ],
        'ip6',
        'mac_address0',
        154
      )
    ],
    Protection20.new(
      false,
      false
    ),
    PublicNet4.new(
      [
        54,
        55,
        56
      ],
      Ipv44.new(
        false,
        'dns_ptr4',
        'ip2',
        104
      ),
      Ipv64.new(
        false,
        [
          DnsPtr8.new(
            'dns_ptr0',
            'ip6'
          ),
          DnsPtr8.new(
            'dns_ptr0',
            'ip6'
          )
        ],
        'ip0',
        8
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
      12.84,
      CpuTypeEnum::SHARED,
      false,
      'description0',
      14.32,
      30,
      21.2,
      'name0',
      [
        Price9.new(
          'location8',
          PriceHourly8.new(
            'gross4',
            'net2'
          ),
          PriceMonthly10.new(
            'gross2',
            'net0'
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



