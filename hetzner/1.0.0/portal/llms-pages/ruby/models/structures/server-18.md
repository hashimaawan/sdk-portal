# Server 18

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcjE4

*This model accepts additional fields of type Object.*


# Class Name

`Server18`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `backup_window` | `String` | Required | Time window (UTC) in which the backup will run, or null if the backups are not enabled |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `datacenter` | [`Datacenter6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/datacenter-6.md) | Required | Datacenter this Resource is located at |
| `id` | `Integer` | Required | ID of the Resource |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/image.md) | Required | - |
| `included_traffic` | `Float` | Required | Free Traffic for the current billing period in bytes |
| `ingoing_traffic` | `Float` | Required | Inbound Traffic for the current billing period in bytes |
| `iso` | [`Iso2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/iso-2.md) | Required | ISO Image that is attached to this Server. Null if no ISO is attached. |
| `labels` | `Hash[String, String]` | Required | User-defined labels (key-value pairs) |
| `load_balancers` | `Array[Integer]` | Optional | - |
| `locked` | `TrueClass \| FalseClass` | Required | True if Server has been locked and is not available to user |
| `name` | `String` | Required | Name of the Server (must be unique per Project and a valid hostname as per RFC 1123) |
| `outgoing_traffic` | `Float` | Required | Outbound Traffic for the current billing period in bytes |
| `placement_group` | [`PlacementGroupNullable`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/placement-group-nullable.md) | Optional | - |
| `primary_disk_size` | `Float` | Required | Size of the primary Disk |
| `private_net` | [`Array[PrivateNet4]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/private-net-4.md) | Required | Private networks information |
| `protection` | [`Protection20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/protection-20.md) | Required | Protection configuration for the Server |
| `public_net` | [`PublicNet4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/public-net-4.md) | Required | Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip` |
| `rescue_enabled` | `TrueClass \| FalseClass` | Required | True if rescue mode is enabled. Server will then boot into rescue system on next reboot |
| `server_type` | [`ServerType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-type-1.md) | Required | Type of Server - determines how much ram, disk and cpu a Server has |
| `status` | [`Status73`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/status-73.md) | Required | Status of the Server |
| `volumes` | `Array[Integer]` | Optional | IDs of Volumes assigned to this Server |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server18 = Server18.new(
  backup_window: '22-02',
  created: '2016-01-30T23:55:00+00:00',
  datacenter: Datacenter6.new(
    description: 'Falkenstein DC Park 8',
    id: 42,
    location: Location.new(
      city: 'Falkenstein',
      country: 'DE',
      description: 'Falkenstein DC Park 1',
      id: 1,
      latitude: 50.47612,
      longitude: 12.370071,
      name: 'fsn1',
      network_zone: 'eu-central',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    name: 'fsn1-dc8',
    server_types: ServerTypes.new(
      available: [
        1,
        2,
        3
      ],
      available_for_migration: [
        1,
        2,
        3
      ],
      supported: [
        1,
        2,
        3
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  id: 42,
  image: Image.new(
    bound_to: nil,
    created: '2016-01-30T23:55:00+00:00',
    created_from: CreatedFrom.new(
      id: 1,
      name: 'Server',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    deleted: nil,
    deprecated: '2018-02-28T00:00:00+00:00',
    description: 'Ubuntu 20.04 Standard 64 bit',
    disk_size: 10,
    id: 42,
    image_size: 2.3,
    labels: {
      'key0' => 'labels4'
    },
    name: 'ubuntu-20.04',
    os_flavor: OsFlavor::UBUNTU,
    os_version: '20.04',
    protection: Protection.new(
      delete: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    status: Status24::UNAVAILABLE,
    type: Type22::SNAPSHOT,
    rapid_deploy: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  included_traffic: 654321,
  ingoing_traffic: 123456,
  iso: Iso2.new(
    deprecated: '2018-02-28T00:00:00+00:00',
    description: 'FreeBSD 11.0 x64',
    id: 42,
    name: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
    type: Type26::PUBLIC,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  labels: {
    'key0' => 'labels4',
    'key1' => 'labels3',
    'key2' => 'labels2'
  },
  locked: false,
  name: 'my-resource',
  outgoing_traffic: 123456,
  primary_disk_size: 50,
  private_net: [
    PrivateNet4.new(
      alias_ips: [
        'alias_ips4'
      ],
      ip: '10.0.0.2',
      mac_address: '86:00:ff:2a:7d:e1',
      network: 4711,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  protection: Protection20.new(
    delete: false,
    rebuild: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  public_net: PublicNet4.new(
    floating_ips: [
      478
    ],
    ipv4: Ipv44.new(
      blocked: false,
      dns_ptr: 'server01.example.com',
      ip: '1.2.3.4',
      id: 42,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    ipv6: Ipv64.new(
      blocked: false,
      dns_ptr: [
        DnsPtr8.new(
          dns_ptr: 'server.example.com',
          ip: '2001:db8::1',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      ip: '2001:db8::/64',
      id: 42,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    firewalls: [
      ServerPublicNetFirewall.new(
        id: 250,
        status: Status72::APPLIED,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      ServerPublicNetFirewall.new(
        id: 250,
        status: Status72::APPLIED,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  rescue_enabled: false,
  server_type: ServerType1.new(
    cores: 1,
    cpu_type: CpuType::SHARED,
    deprecated: false,
    description: 'CX11',
    disk: 25,
    id: 1,
    memory: 1,
    name: 'cx11',
    prices: [
      Price9.new(
        location: 'fsn1',
        price_hourly: PriceHourly8.new(
          gross: '1.1900000000000000',
          net: '1.0000000000',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        price_monthly: PriceMonthly10.new(
          gross: '1.1900000000000000',
          net: '1.0000000000',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    storage_type: StorageType::LOCAL,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  status: Status73::RUNNING,
  load_balancers: [
    248
  ],
  placement_group: PlacementGroupNullable.new(
    created: 'created8',
    id: 236,
    labels: {
      'key0' => 'labels4'
    },
    name: 'name8',
    servers: [
      251,
      252,
      253
    ],
    type: 'type2',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  volumes: [
    199,
    200,
    201
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



