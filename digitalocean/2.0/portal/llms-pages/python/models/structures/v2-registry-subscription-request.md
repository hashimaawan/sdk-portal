# V2 Registry Subscription Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwU3Vic2NyaXB0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2RegistrySubscriptionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tier_slug` | [`TierSlug`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/tier-slug.md) | Optional | The slug of the subscription tier to sign up for. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.tier_slug import TierSlug
from digitaloceanapi.models.v_2_registry_subscription_request import V2RegistrySubscriptionRequest

v_2_registry_subscription_request = V2RegistrySubscriptionRequest(
    tier_slug=TierSlug.BASIC,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



