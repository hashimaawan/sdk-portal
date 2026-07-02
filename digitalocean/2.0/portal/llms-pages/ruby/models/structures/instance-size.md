# Instance Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkluc3RhbmNlU2l6ZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`InstanceSize`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cpu_type` | [`MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/shared-shared-v-cpu-cores-dedicated-dedicated-v-cpu-cores.md) | Optional | **Default**: `MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores::UNSPECIFIED` |
| `cpus` | `String` | Optional | - |
| `memory_bytes` | `String` | Optional | - |
| `name` | `String` | Optional | - |
| `slug` | `String` | Optional | - |
| `tier_downgrade_to` | `String` | Optional | - |
| `tier_slug` | `String` | Optional | - |
| `tier_upgrade_to` | `String` | Optional | - |
| `usd_per_month` | `String` | Optional | - |
| `usd_per_second` | `String` | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
instance_size = InstanceSize.new(
  cpu_type: MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores::SHARED,
  cpus: '3',
  memory_bytes: '1048',
  name: 'name',
  slug: 'basic',
  tier_downgrade_to: 'basic',
  tier_slug: 'basic',
  tier_upgrade_to: 'basic',
  usd_per_month: '23',
  usd_per_second: '0.00000001232',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



