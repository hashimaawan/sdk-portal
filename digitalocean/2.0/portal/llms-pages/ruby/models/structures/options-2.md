# Options 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk9wdGlvbnMy

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Options2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available_regions` | `Array[String]` | Optional | - |
| `subscription_tiers` | [`Array[SubscriptionTier]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/subscription-tier.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
options2 = Options2.new(
  available_regions: [
    'nyc3'
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
)
```



