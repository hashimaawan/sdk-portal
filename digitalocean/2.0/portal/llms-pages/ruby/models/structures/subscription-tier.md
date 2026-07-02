# Subscription Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvblRpZXI

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`SubscriptionTier`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allow_storage_overage` | `TrueClass \| FalseClass` | Optional | A boolean indicating whether the subscription tier supports additional storage above what is included in the base plan at an additional cost per GiB used. |
| `included_bandwidth_bytes` | `Integer` | Optional | The amount of outbound data transfer included in the subscription tier in bytes. |
| `included_repositories` | `Integer` | Optional | The number of repositories included in the subscription tier. `0` indicates that the subscription tier includes unlimited repositories. |
| `included_storage_bytes` | `Integer` | Optional | The amount of storage included in the subscription tier in bytes. |
| `monthly_price_in_cents` | `Integer` | Optional | The monthly cost of the subscription tier in cents. |
| `name` | `String` | Optional | The name of the subscription tier. |
| `slug` | `String` | Optional | The slug identifier of the subscription tier. |
| `storage_overage_price_in_cents` | `Integer` | Optional | The price paid in cents per GiB for additional storage beyond what is included in the subscription plan. |
| `eligibility_reasons` | [`Array[EligibilityReason]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/eligibility-reason.md) | Optional | If your account is not eligible to use a certain subscription tier, this will include a list of reasons that prevent you from using the tier. |
| `eligible` | `TrueClass \| FalseClass` | Optional | A boolean indicating whether your account it eligible to use a certain subscription tier. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
subscription_tier = SubscriptionTier.new(
  allow_storage_overage: true,
  included_bandwidth_bytes: 5368709120,
  included_repositories: 5,
  included_storage_bytes: 5368709120,
  monthly_price_in_cents: 500,
  name: 'Basic',
  slug: 'basic',
  storage_overage_price_in_cents: 2,
  eligibility_reasons: [
    EligibilityReason::OVERREPOSITORYLIMIT
  ],
  eligible: true,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



