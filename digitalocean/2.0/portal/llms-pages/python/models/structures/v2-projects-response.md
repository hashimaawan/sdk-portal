# V2 Projects Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2ProjectsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projects` | [`List[Project]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/project.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.environment import Environment
from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.project import Project
from digitaloceanapi.models.v_2_projects_response import V2ProjectsResponse

v_2_projects_response = V2ProjectsResponse(
    meta=Meta(
        total=2,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    projects=[
        Project(
            created_at=dateutil.parser.parse('2018-09-27T20:10:35Z'),
            description='My website API',
            environment=Environment.PRODUCTION,
            id='4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679',
            name='my-web-api',
            owner_id=258992,
            owner_uuid='99525febec065ca37b2ffe4f852fd2b2581895e7',
            purpose='Service or API',
            updated_at=dateutil.parser.parse('2018-09-27T20:10:35Z'),
            is_default=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Project(
            created_at=dateutil.parser.parse('2017-10-19T21:44:20Z'),
            description='Default project',
            environment=Environment.DEVELOPMENT,
            id='addb4547-6bab-419a-8542-76263a033cf6',
            name='Default',
            owner_id=258992,
            owner_uuid='99525febec065ca37b2ffe4f852fd2b2581895e7',
            purpose='Just trying out DigitalOcean',
            updated_at=dateutil.parser.parse('2019-11-05T18:50:03Z'),
            is_default=True,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    links=Links(
        pages=Pages(
            last='https://api.digitalocean.com/v2/projects?page=1',
            next='next2',
            additional_properties={
                'first': jsonpickle.decode('"https://api.digitalocean.com/v2/projects?page=1"')
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



