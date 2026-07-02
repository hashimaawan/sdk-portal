# Subscription

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvbg

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Subscription`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional, Read-only | The time at which the subscription was created. |
| `tier` | [`Tier1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/tier-1.md) | Optional | - |
| `updated_at` | `datetime` | Optional, Read-only | The time at which the subscription was last updated. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.subscription import Subscription
from digitaloceanapi.models.tier_1 import Tier1

subscription = Subscription(
    created_at=dateutil.parser.parse('2020-01-23T21:19:12Z'),
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
    updated_at=dateutil.parser.parse('2020-11-05T15:53:24Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



