# V2 Droplets Destroy with Associated Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floating_ips` | [`Array[FloatingIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/floating-ip.md) | Optional | - |
| `reserved_ips` | [`Array[FloatingIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/floating-ip.md) | Optional | - |
| `snapshots` | [`Array[FloatingIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/floating-ip.md) | Optional | - |
| `volume_snapshots` | [`Array[FloatingIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/floating-ip.md) | Optional | - |
| `volumes` | [`Array[FloatingIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/floating-ip.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_droplets_destroy_with_associated_resources_response = V2DropletsDestroyWithAssociatedResourcesResponse.new(
  floating_ips: [
    FloatingIp.new(
      cost: 'cost0',
      id: 'id2',
      name: 'name2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    FloatingIp.new(
      cost: 'cost0',
      id: 'id2',
      name: 'name2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  reserved_ips: [
    FloatingIp.new(
      cost: 'cost8',
      id: 'id0',
      name: 'name0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  snapshots: [
    FloatingIp.new(
      cost: 'cost0',
      id: 'id2',
      name: 'name2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    FloatingIp.new(
      cost: 'cost0',
      id: 'id2',
      name: 'name2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  volume_snapshots: [
    FloatingIp.new(
      cost: 'cost6',
      id: 'id8',
      name: 'name8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  volumes: [
    FloatingIp.new(
      cost: 'cost4',
      id: 'id6',
      name: 'name6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    FloatingIp.new(
      cost: 'cost4',
      id: 'id6',
      name: 'name6',
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



