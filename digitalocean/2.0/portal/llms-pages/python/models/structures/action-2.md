# Action 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkFjdGlvbjI

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Action2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `completed_at` | `datetime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. |
| `id` | `int` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/region.md) | Optional | - |
| `region_slug` | `str` | Optional | - |
| `resource_id` | `int` | Optional | A unique identifier for the resource that the action is associated with. |
| `resource_type` | `str` | Optional | The type of resource that the action is associated with. |
| `started_at` | `datetime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `"in-progress"` |
| `mtype` | `str` | Optional | This is the type of action that the object represents. For example, this could be "transfer" to represent the state of an image transfer action. |
| `project_id` | `uuid\|str` | Optional | The UUID of the project to which the reserved IP currently belongs. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.action_2 import Action2
from digitaloceanapi.models.region import Region
from digitaloceanapi.models.status_1 import Status1

action_2 = Action2(
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
    region_slug='region_slug4',
    resource_id=3164444,
    resource_type='droplet',
    started_at=dateutil.parser.parse('2020-11-14T16:29:21Z'),
    status=Status1.COMPLETED,
    mtype='create',
    project_id='746c6152-2fa2-11ed-92d3-27aaa54e4988',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



