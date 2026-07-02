# Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkNoZWNr

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Check`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Optional, Read-only | A unique ID that can be used to identify and reference the check. |
| `enabled` | `bool` | Optional | A boolean value indicating whether the check is enabled/disabled.<br><br>**Default**: `True` |
| `name` | `str` | Optional | A human-friendly display name. |
| `regions` | [`List[Region8]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/region-8.md) | Optional | An array containing the selected regions to perform healthchecks from. |
| `target` | `str` | Optional | The endpoint to perform healthchecks on. |
| `mtype` | [`Type19`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-19.md) | Optional | The type of health check to perform. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.check import Check
from digitaloceanapi.models.region_8 import Region8
from digitaloceanapi.models.type_19 import Type19

check = Check(
    id='5a4981aa-9653-4bd1-bef5-d6bff52042e4',
    enabled=True,
    name='Landing page check',
    regions=[
        Region8.US_EAST,
        Region8.EU_WEST
    ],
    target='https://www.landingpage.com',
    mtype=Type19.HTTPS,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



