# V2 Volumes Actions Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2VolumesActionsRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/region-2.md) | Optional | The slug identifier for the region where the resource will initially be  available. |
| `mtype` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-21.md) | Required | The volume action to initiate. |
| `size_gigabytes` | `int` | Required | The new size of the block storage volume in GiB (1024^3).<br><br>**Constraints**: `<= 16384` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.region_2 import Region2
from digitaloceanapi.models.type_21 import Type21
from digitaloceanapi.models.v_2_volumes_actions_request_2 import V2VolumesActionsRequest2

v_2_volumes_actions_request_2 = V2VolumesActionsRequest2(
    mtype=Type21.ATTACH,
    size_gigabytes=15384,
    region=Region2.NYC3,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



