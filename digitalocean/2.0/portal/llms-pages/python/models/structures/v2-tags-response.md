# V2 Tags Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2TagsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tags` | [`List[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/tag.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.databases import Databases
from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.resources_2 import Resources2
from digitaloceanapi.models.tag import Tag
from digitaloceanapi.models.v_2_tags_response import V2TagsResponse

v_2_tags_response = V2TagsResponse(
    meta=Meta(
        total=1,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    tags=[
        Tag(
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
    ],
    links=Links(
        pages=Pages(
            last='last6',
            next='next2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
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



