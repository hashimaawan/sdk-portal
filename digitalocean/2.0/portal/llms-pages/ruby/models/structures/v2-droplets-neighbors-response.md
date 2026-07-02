# V2 Droplets Neighbors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwTmVpZ2hib3JzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DropletsNeighborsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplets` | [`Array[Droplet]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/droplet.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_droplets_neighbors_response = V2DropletsNeighborsResponse.new(
  droplets: [
    Droplet.new(
      backup_ids: [
        104,
        105
      ],
      created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      disk: 98,
      features: [
        'features1',
        'features2',
        'features3'
      ],
      id: 232,
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
      memory: 16,
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
        93,
        94
      ],
      status: Status8::NEW,
      tags: [
        'tags5'
      ],
      vcpus: 80,
      volume_ids: [
        'volume_ids0',
        'volume_ids1',
        'volume_ids2'
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
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



