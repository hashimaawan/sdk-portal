# V2 Apps Tiers Instance Sizes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsTiersInstanceSizesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `discount_percent` | `Float` | Optional | - |
| `instance_sizes` | [`Array[InstanceSize]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/instance-size.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_tiers_instance_sizes_response = V2AppsTiersInstanceSizesResponse.new(
  discount_percent: 2.32,
  instance_sizes: [
    InstanceSize.new(
      cpu_type: MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores::DEDICATED,
      cpus: 'cpus4',
      memory_bytes: 'memory_bytes8',
      name: 'name8',
      slug: 'slug8',
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



