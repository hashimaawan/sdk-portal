# V2 Droplets Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DropletsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet` | [`Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/droplet.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_droplets_response1 = V2DropletsResponse1.new(
  droplet: Droplet.new(
    backup_ids: [
      156,
      157,
      158
    ],
    created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    disk: 150,
    features: [
      'features1'
    ],
    id: 28,
    image: Image1.new(
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      description: 'description6',
      distribution: Distribution::COREOS,
      error_message: 'error_message8',
      id: 128,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    locked: false,
    memory: 64,
    name: 'name0',
    networks: Networks.new(
      v4: [
        V4.new(
          gateway: 'gateway2',
          ip_address: 'ip_address2',
          netmask: 'netmask2',
          type: Type10::PUBLIC,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        V4.new(
          gateway: 'gateway2',
          ip_address: 'ip_address2',
          netmask: 'netmask2',
          type: Type10::PUBLIC,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        V4.new(
          gateway: 'gateway2',
          ip_address: 'ip_address2',
          netmask: 'netmask2',
          type: Type10::PUBLIC,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      v6: [
        V6.new(
          gateway: 'gateway4',
          ip_address: 'ip_address4',
          netmask: 106,
          type: Type11::PUBLIC,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        V6.new(
          gateway: 'gateway4',
          ip_address: 'ip_address4',
          netmask: 106,
          type: Type11::PUBLIC,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    next_backup_window: NextBackupWindow.new(
      mend: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      start: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    region: Region.new(
      available: false,
      features: [
        'features7',
        'features8',
        'features9'
      ],
      name: 'name6',
      sizes: [
        'sizes6'
      ],
      slug: 'slug0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    size: Size.new(
      available: false,
      description: 'description0',
      disk: 252,
      memory: 168,
      price_hourly: 121.04,
      price_monthly: 162.04,
      regions: [
        'regions5'
      ],
      slug: 'slug6',
      transfer: 150.78,
      vcpus: 234,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    size_slug: 'size_slug0',
    snapshot_ids: [
      145,
      146,
      147
    ],
    status: Status8::NEW,
    tags: [
      'tags5',
      'tags6'
    ],
    vcpus: 132,
    volume_ids: [
      'volume_ids0'
    ],
    kernel: Kernel.new(
      id: 16,
      name: 'name4',
      version: 'version0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    vpc_uuid: 'vpc_uuid0',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



