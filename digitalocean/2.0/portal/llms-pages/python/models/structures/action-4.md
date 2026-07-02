# Action 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkFjdGlvbjQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Action4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_id` | `int` | Optional | A unique identifier for the resource that the action is associated with. |
| `mtype` | `str` | Optional | This is the type of action that the object represents. For example, this could be "attach_volume" to represent the state of a volume attach action. |
| `completed_at` | `datetime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. |
| `id` | `int` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/region.md) | Optional | - |
| `region_slug` | `str` | Optional | - |
| `resource_type` | `str` | Optional | The type of resource that the action is associated with. |
| `started_at` | `datetime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `"in-progress"` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.action_4 import Action4
from digitaloceanapi.models.region import Region
from digitaloceanapi.models.status_1 import Status1

action_4 = Action4(
    resource_id=96,
    mtype='attach_volume',
    completed_at=dateutil.parser.parse('2020-11-14T16:30:06Z'),
    id=36804636,
    region=Region(
        available=False,
        features=[
            'features7',
            'features8',
            'features9'
        ],
        name='name6',
        sizes=[
            'sizes6'
        ],
        slug='slug0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    resource_type='droplet',
    started_at=dateutil.parser.parse('2020-11-14T16:29:21Z'),
    status=Status1.COMPLETED,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



