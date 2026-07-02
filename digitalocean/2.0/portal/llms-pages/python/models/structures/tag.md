# Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlRhZw

A tag is a label that can be applied to a resource (currently Droplets, Images, Volumes, Volume Snapshots, and Database clusters) in order to better organize or facilitate the lookups and actions on it.
Tags have two attributes: a user defined `name` attribute and an embedded `resources` attribute with information about resources that have been tagged.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Tag`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | The name of the tag. Tags may contain letters, numbers, colons, dashes, and underscores.<br>There is a limit of 255 characters per tag.<br><br>**Note:** Tag names are case stable, which means the capitalization you use when you first create a tag is canonical.<br><br>When working with tags in the API, you must use the tag's canonical capitalization. For example, if you create a tag named "PROD", the URL to add that tag to a resource would be `https://api.digitalocean.com/v2/tags/PROD/resources` (not `/v2/tags/prod/resources`).<br><br>Tagged resources in the control panel will always display the canonical capitalization. For example, if you create a tag named "PROD", you can tag resources in the control panel by entering "prod". The tag will still display with its canonical capitalization, "PROD".<br><br>**Constraints**: *Maximum Length*: `255`, *Pattern*: `^[a-zA-Z0-9_\-\:]+$` |
| `resources` | [`Resources2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/resources-2.md) | Optional, Read-only | An embedded object containing key value pairs of resource type and resource statistics. It also includes a count of the total number of resources tagged with the current tag as well as a `last_tagged_uri` attribute set to the last resource tagged with the current tag. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.databases import Databases
from digitaloceanapi.models.resources_2 import Resources2
from digitaloceanapi.models.tag import Tag

tag = Tag(
    name='extra-awesome',
    resources=Resources2(
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
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



