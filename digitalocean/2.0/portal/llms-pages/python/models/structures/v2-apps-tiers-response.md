# V2 Apps Tiers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsTiersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tiers` | [`List[Tier]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/tier.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.tier import Tier
from digitaloceanapi.models.v_2_apps_tiers_response import V2AppsTiersResponse

v_2_apps_tiers_response = V2AppsTiersResponse(
    tiers=[
        Tier(
            build_seconds='build_seconds4',
            egress_bandwidth_bytes='egress_bandwidth_bytes2',
            name='name8',
            slug='slug8',
            storage_bytes='storage_bytes4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Tier(
            build_seconds='build_seconds4',
            egress_bandwidth_bytes='egress_bandwidth_bytes2',
            name='name8',
            slug='slug8',
            storage_bytes='storage_bytes4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Tier(
            build_seconds='build_seconds4',
            egress_bandwidth_bytes='egress_bandwidth_bytes2',
            name='name8',
            slug='slug8',
            storage_bytes='storage_bytes4',
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



