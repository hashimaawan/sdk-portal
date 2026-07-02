# V2 Projects Default Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2ProjectsDefaultResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `project` | [`Project`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/project.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.environment import Environment
from digitaloceanapi.models.project import Project
from digitaloceanapi.models.v_2_projects_default_response import V2ProjectsDefaultResponse

v_2_projects_default_response = V2ProjectsDefaultResponse(
    project=Project(
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
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



