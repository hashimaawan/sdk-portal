# V2 Tags Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2TagsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tag` | [`Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/tag.md) | Optional | A tag is a label that can be applied to a resource (currently Droplets, Images, Volumes, Volume Snapshots, and Database clusters) in order to better organize or facilitate the lookups and actions on it.<br>Tags have two attributes: a user defined `name` attribute and an embedded `resources` attribute with information about resources that have been tagged. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.databases import Databases
from digitaloceanapi.models.resources_2 import Resources2
from digitaloceanapi.models.tag import Tag
from digitaloceanapi.models.v_2_tags_response_1 import V2TagsResponse1

v_2_tags_response_1 = V2TagsResponse1(
    tag=Tag(
        name='extra-awesome',
        resources=Resources2(
            count=0,
            last_tagged_uri='last_tagged_uri6',
            databases=Databases(
                count=0,
                last_tagged_uri='last_tagged_uri2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            droplets=Databases(
                count=0,
                last_tagged_uri='last_tagged_uri6',
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
                count=0
            ),
            volumes=Databases(
                count=0
            ),
            additional_properties={
                'images': jsonpickle.decode('{"count":0}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



