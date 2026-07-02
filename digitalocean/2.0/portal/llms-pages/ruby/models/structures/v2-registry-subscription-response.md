# V2 Registry Subscription Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwU3Vic2NyaXB0aW9uJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2RegistrySubscriptionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `subscription` | [`Subscription`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/subscription.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_registry_subscription_response = V2RegistrySubscriptionResponse.new(
  subscription: Subscription.new(
    created_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
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
    updated_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



