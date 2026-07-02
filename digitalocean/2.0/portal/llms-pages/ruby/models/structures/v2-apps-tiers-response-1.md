# V2 Apps Tiers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsTiersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tier` | [`Tier`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/tier.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_tiers_response1 = V2AppsTiersResponse1.new(
  tier: Tier.new(
    build_seconds: 'build_seconds0',
    egress_bandwidth_bytes: 'egress_bandwidth_bytes6',
    name: 'name2',
    slug: 'slug4',
    storage_bytes: 'storage_bytes0',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



