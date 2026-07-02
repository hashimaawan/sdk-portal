# Subscription

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvbg

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Subscription`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `DateTime` | Optional, Read-only | The time at which the subscription was created. |
| `tier` | [`Tier1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/tier-1.md) | Optional | - |
| `updated_at` | `DateTime` | Optional, Read-only | The time at which the subscription was last updated. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
subscription = Subscription.new(
  created_at: DateTimeHelper.from_rfc3339('2020-01-23T21:19:12Z'),
  tier: Tier1.new(
    allow_storage_overage: false,
    included_bandwidth_bytes: 46,
    included_repositories: 68,
    included_storage_bytes: 112,
    monthly_price_in_cents: 110,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  updated_at: DateTimeHelper.from_rfc3339('2020-11-05T15:53:24Z'),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



