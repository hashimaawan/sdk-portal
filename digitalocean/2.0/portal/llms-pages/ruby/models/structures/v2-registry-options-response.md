# V2 Registry Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwT3B0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2RegistryOptionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `options` | [`Options2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/options-2.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_registry_options_response = V2RegistryOptionsResponse.new(
  options: Options2.new(
    available_regions: [
      'available_regions9'
    ],
    subscription_tiers: [
      SubscriptionTier.new(
        allow_storage_overage: false,
        included_bandwidth_bytes: 172,
        included_repositories: 194,
        included_storage_bytes: 242,
        monthly_price_in_cents: 236,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      SubscriptionTier.new(
        allow_storage_overage: false,
        included_bandwidth_bytes: 172,
        included_repositories: 194,
        included_storage_bytes: 242,
        monthly_price_in_cents: 236,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      SubscriptionTier.new(
        allow_storage_overage: false,
        included_bandwidth_bytes: 172,
        included_repositories: 194,
        included_storage_bytes: 242,
        monthly_price_in_cents: 236,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
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



