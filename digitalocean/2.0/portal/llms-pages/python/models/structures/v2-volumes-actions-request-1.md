# V2 Volumes Actions Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2VolumesActionsRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/region-2.md) | Optional | The slug identifier for the region where the resource will initially be  available. |
| `mtype` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-21.md) | Required | The volume action to initiate. |
| `droplet_id` | `int` | Required | The unique identifier for the Droplet the volume will be attached or detached from. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.region_2 import Region2
from digitaloceanapi.models.type_21 import Type21
from digitaloceanapi.models.v_2_volumes_actions_request_1 import V2VolumesActionsRequest1

v_2_volumes_actions_request_1 = V2VolumesActionsRequest1(
    mtype=Type21.ATTACH,
    droplet_id=11612190,
    region=Region2.NYC3,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



