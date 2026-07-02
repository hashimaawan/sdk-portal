# Options 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRk9wdGlvbnMy

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Options2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available_regions` | `List[str]` | Optional | - |
| `subscription_tiers` | [`List[SubscriptionTier]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/subscription-tier.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.options_2 import Options2
from digitaloceanapi.models.subscription_tier import SubscriptionTier

options_2 = Options2(
    available_regions=[
        'nyc3'
    ],
    subscription_tiers=[
        SubscriptionTier(
            allow_storage_overage=False,
            included_bandwidth_bytes=172,
            included_repositories=194,
            included_storage_bytes=242,
            monthly_price_in_cents=236,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        SubscriptionTier(
            allow_storage_overage=False,
            included_bandwidth_bytes=172,
            included_repositories=194,
            included_storage_bytes=242,
            monthly_price_in_cents=236,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        SubscriptionTier(
            allow_storage_overage=False,
            included_bandwidth_bytes=172,
            included_repositories=194,
            included_storage_bytes=242,
            monthly_price_in_cents=236,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



