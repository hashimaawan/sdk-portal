# V2 Registry Subscription Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwU3Vic2NyaXB0aW9uJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2RegistrySubscriptionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `subscription` | [`Subscription`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/subscription.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.subscription import Subscription
from digitaloceanapi.models.tier_1 import Tier1
from digitaloceanapi.models.v_2_registry_subscription_response import V2RegistrySubscriptionResponse

v_2_registry_subscription_response = V2RegistrySubscriptionResponse(
    subscription=Subscription(
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        tier=Tier1(
            allow_storage_overage=False,
            included_bandwidth_bytes=46,
            included_repositories=68,
            included_storage_bytes=112,
            monthly_price_in_cents=110,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        updated_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



