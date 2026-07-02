# V2 Registry Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwT3B0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2RegistryOptionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `options` | [`Options2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/options-2.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.options_2 import Options2
from digitaloceanapi.models.subscription_tier import SubscriptionTier
from digitaloceanapi.models.v_2_registry_options_response import V2RegistryOptionsResponse

v_2_registry_options_response = V2RegistryOptionsResponse(
    options=Options2(
        available_regions=[
            'available_regions9'
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
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



