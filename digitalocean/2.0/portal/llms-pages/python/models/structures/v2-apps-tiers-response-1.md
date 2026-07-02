# V2 Apps Tiers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsTiersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tier` | [`Tier`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/tier.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.tier import Tier
from digitaloceanapi.models.v_2_apps_tiers_response_1 import V2AppsTiersResponse1

v_2_apps_tiers_response_1 = V2AppsTiersResponse1(
    tier=Tier(
        build_seconds='build_seconds0',
        egress_bandwidth_bytes='egress_bandwidth_bytes6',
        name='name2',
        slug='slug4',
        storage_bytes='storage_bytes0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



