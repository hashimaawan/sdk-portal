# Subscription Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvblRpZXI

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`SubscriptionTier`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allow_storage_overage` | `bool` | Optional | A boolean indicating whether the subscription tier supports additional storage above what is included in the base plan at an additional cost per GiB used. |
| `included_bandwidth_bytes` | `int` | Optional | The amount of outbound data transfer included in the subscription tier in bytes. |
| `included_repositories` | `int` | Optional | The number of repositories included in the subscription tier. `0` indicates that the subscription tier includes unlimited repositories. |
| `included_storage_bytes` | `int` | Optional | The amount of storage included in the subscription tier in bytes. |
| `monthly_price_in_cents` | `int` | Optional | The monthly cost of the subscription tier in cents. |
| `name` | `str` | Optional | The name of the subscription tier. |
| `slug` | `str` | Optional | The slug identifier of the subscription tier. |
| `storage_overage_price_in_cents` | `int` | Optional | The price paid in cents per GiB for additional storage beyond what is included in the subscription plan. |
| `eligibility_reasons` | [`List[EligibilityReason]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/eligibility-reason.md) | Optional | If your account is not eligible to use a certain subscription tier, this will include a list of reasons that prevent you from using the tier. |
| `eligible` | `bool` | Optional | A boolean indicating whether your account it eligible to use a certain subscription tier. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.eligibility_reason import EligibilityReason
from digitaloceanapi.models.subscription_tier import SubscriptionTier

subscription_tier = SubscriptionTier(
    allow_storage_overage=True,
    included_bandwidth_bytes=5368709120,
    included_repositories=5,
    included_storage_bytes=5368709120,
    monthly_price_in_cents=500,
    name='Basic',
    slug='basic',
    storage_overage_price_in_cents=2,
    eligibility_reasons=[
        EligibilityReason.OVERREPOSITORYLIMIT
    ],
    eligible=True,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



