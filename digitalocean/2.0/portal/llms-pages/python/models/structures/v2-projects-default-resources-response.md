# V2 Projects Default Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2ProjectsDefaultResourcesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resources` | [`List[Resources1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/resources-1.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.links import Links
from digitaloceanapi.models.links_4 import Links4
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.resources_1 import Resources1
from digitaloceanapi.models.status_14 import Status14
from digitaloceanapi.models.v_2_projects_default_resources_response import V2ProjectsDefaultResourcesResponse

v_2_projects_default_resources_response = V2ProjectsDefaultResourcesResponse(
    meta=Meta(
        total=2,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    resources=[
        Resources1(
            assigned_at=dateutil.parser.parse('2018-09-28T19:26:37Z'),
            links=Links4(
                mself='https://api.digitalocean.com/v2/droplets/13457723',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            status=Status14.OK,
            urn='do:droplet:13457723',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Resources1(
            assigned_at=dateutil.parser.parse('2019-03-31T16:24:14Z'),
            links=Links4(
                mself='https://api.digitalocean.com/v2/domains/example.com',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            status=Status14.OK,
            urn='do:domain:example.com',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    links=Links(
        pages=Pages(
            last='https://api.digitalocean.com/v2/projects/4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679/resources?page=1',
            next='next2',
            additional_properties={
                'first': jsonpickle.decode('"https://api.digitalocean.com/v2/projects/4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679/resources?page=1"')
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



