# V2 Apps Tiers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsTiersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tiers` | [`Array[Tier]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/tier.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_tiers_response = V2AppsTiersResponse.new(
  tiers: [
    Tier.new(
      build_seconds: 'build_seconds4',
      egress_bandwidth_bytes: 'egress_bandwidth_bytes2',
      name: 'name8',
      slug: 'slug8',
      storage_bytes: 'storage_bytes4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Tier.new(
      build_seconds: 'build_seconds4',
      egress_bandwidth_bytes: 'egress_bandwidth_bytes2',
      name: 'name8',
      slug: 'slug8',
      storage_bytes: 'storage_bytes4',
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



