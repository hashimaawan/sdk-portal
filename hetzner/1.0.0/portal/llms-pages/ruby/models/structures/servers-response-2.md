# Servers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type Object.*


# Class Name

`ServersResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-18.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
servers_response2 = ServersResponse2.new(
  server: Server18.new(
    backup_window: 'backup_window2',
    created: 'created4',
    datacenter: Datacenter6.new(
      description: 'description0',
      id: 200,
      location: Location.new(
        city: 'city6',
        country: 'country8',
        description: 'description6',
        id: 187.14,
        latitude: 194.62,
        longitude: 59.18,
        name: 'name4',
        network_zone: 'network_zone2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      name: 'name0',
      server_types: ServerTypes.new(
        available: [
          23.74
        ],
        available_for_migration: [
          201.65,
          201.66
        ],
        supported: [
          69.52,
          69.53,
          69.54
        ],
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    id: 14,
    image: Image.new(
      bound_to: 186,
      created: 'created6',
      created_from: CreatedFrom.new(
        id: 60,
        name: 'name6',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      deleted: 'deleted4',
      deprecated: 'deprecated8',
      description: 'description6',
      disk_size: 244.18,
      id: 128,
      image_size: 141.34,
      labels: {
        'key0' => 'labels4'
      },
      name: 'name6',
      os_flavor: OsFlavor::DEBIAN,
      os_version: 'os_version4',
      protection: Protection.new(
        delete: false,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      status: Status24::UNAVAILABLE,
      type: Type22::APP,
      rapid_deploy: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    included_traffic: 123.68,
    ingoing_traffic: 151.82,
    iso: Iso2.new(
      deprecated: 'deprecated0',
      description: 'description2',
      id: 66,
      name: 'name8',
      type: Type26::PUBLIC,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    labels: {
      'key0' => 'labels0',
      'key1' => 'labels9'
    },
    locked: false,
    name: 'name4',
    outgoing_traffic: 129.6,
    primary_disk_size: 19.88,
    private_net: [
      PrivateNet4.new(
        alias_ips: [
          'alias_ips4'
        ],
        ip: 'ip6',
        mac_address: 'mac_address0',
        network: 154,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      PrivateNet4.new(
        alias_ips: [
          'alias_ips4'
        ],
        ip: 'ip6',
        mac_address: 'mac_address0',
        network: 154,
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
        54,
        55,
        56
      ],
      ipv4: Ipv44.new(
        blocked: false,
        dns_ptr: 'dns_ptr4',
        ip: 'ip2',
        id: 104,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      ipv6: Ipv64.new(
        blocked: false,
        dns_ptr: [
          DnsPtr8.new(
            dns_ptr: 'dns_ptr0',
            ip: 'ip6',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          DnsPtr8.new(
            dns_ptr: 'dns_ptr0',
            ip: 'ip6',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          )
        ],
        ip: 'ip0',
        id: 8,
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
      cores: 12.84,
      cpu_type: CpuType::SHARED,
      deprecated: false,
      description: 'description0',
      disk: 14.32,
      id: 30,
      memory: 21.2,
      name: 'name0',
      prices: [
        Price9.new(
          location: 'location8',
          price_hourly: PriceHourly8.new(
            gross: 'gross4',
            net: 'net2',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          price_monthly: PriceMonthly10.new(
            gross: 'gross2',
            net: 'net0',
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
    status: Status73::STARTING,
    load_balancers: [
      144,
      143,
      142
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
      91,
      92
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



