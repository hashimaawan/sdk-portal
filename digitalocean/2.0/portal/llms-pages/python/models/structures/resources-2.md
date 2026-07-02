# Resources 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlc291cmNlczI

An embedded object containing key value pairs of resource type and resource statistics. It also includes a count of the total number of resources tagged with the current tag as well as a `last_tagged_uri` attribute set to the last resource tagged with the current tag.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Resources2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `count` | `int` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` |
| `last_tagged_uri` | `str` | Optional | The URI for the last tagged object for this type of resource. |
| `databases` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `droplets` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `imgages` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `volume_snapshots` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `volumes` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.databases import Databases
from digitaloceanapi.models.resources_2 import Resources2

resources_2 = Resources2(
    count=5,
    last_tagged_uri='https://api.digitalocean.com/v2/images/7555620',
    databases=Databases(
        count=1,
        last_tagged_uri='https://api.digitalocean.com/v2/databases/b92438f6-ba03-416c-b642-e9236db91976',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    droplets=Databases(
        count=1,
        last_tagged_uri='https://api.digitalocean.com/v2/droplets/3164444',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    imgages=Databases(
        count=158,
        last_tagged_uri='last_tagged_uri4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    volume_snapshots=Databases(
        count=1,
        last_tagged_uri='https://api.digitalocean.com/v2/snapshots/1f6f46e8-6b60-11e9-be4e-0a58ac144519'
    ),
    volumes=Databases(
        count=1,
        last_tagged_uri='https://api.digitalocean.com/v2/volumes/3d80cb72-342b-4aaa-b92e-4e4abb24a933'
    ),
    additional_properties={
        'images': jsonpickle.decode('{"count":1,"last_tagged_uri":"https://api.digitalocean.com/v2/images/7555620"}')
    }
)
```



