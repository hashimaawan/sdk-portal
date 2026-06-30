# Server 18

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcjE4


# Class Name

`Server18`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `backup_window` | `String` | Required | Time window (UTC) in which the backup will run, or null if the backups are not enabled |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `datacenter` | [`Datacenter6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/datacenter-6.md) | Required | Datacenter this Resource is located at |
| `id` | `Integer` | Required | ID of the Resource |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/image.md) | Required | - |
| `included_traffic` | `Float` | Required | Free Traffic for the current billing period in bytes |
| `ingoing_traffic` | `Float` | Required | Inbound Traffic for the current billing period in bytes |
| `iso` | [`Iso2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/iso-2.md) | Required | ISO Image that is attached to this Server. Null if no ISO is attached. |
| `labels` | `Hash[String, String]` | Required | User-defined labels (key-value pairs) |
| `load_balancers` | `Array[Integer]` | Optional | - |
| `locked` | `TrueClass \| FalseClass` | Required | True if Server has been locked and is not available to user |
| `name` | `String` | Required | Name of the Server (must be unique per Project and a valid hostname as per RFC 1123) |
| `outgoing_traffic` | `Float` | Required | Outbound Traffic for the current billing period in bytes |
| `placement_group` | [`PlacementGroupNullable`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/placement-group-nullable.md) | Optional | - |
| `primary_disk_size` | `Float` | Required | Size of the primary Disk |
| `private_net` | [`Array[PrivateNet4]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/private-net-4.md) | Required | Private networks information |
| `protection` | [`Protection20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/protection-20.md) | Required | Protection configuration for the Server |
| `public_net` | [`PublicNet4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/public-net-4.md) | Required | Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip` |
| `rescue_enabled` | `TrueClass \| FalseClass` | Required | True if rescue mode is enabled. Server will then boot into rescue system on next reboot |
| `server_type` | [`ServerType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/server-type-1.md) | Required | Type of Server - determines how much ram, disk and cpu a Server has |
| `status` | [`Status73Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/status-73.md) | Required | Status of the Server |
| `volumes` | `Array[Integer]` | Optional | IDs of Volumes assigned to this Server |


# Example

```ruby
server18 = Server18.new(
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
    'key0': 'labels4',
    'key1': 'labels3',
    'key2': 'labels2'
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
  Status73Enum::RUNNING,
  [
    248
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
    199,
    200,
    201
  ]
)
```



