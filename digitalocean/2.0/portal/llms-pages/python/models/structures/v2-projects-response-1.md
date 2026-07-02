# V2 Projects Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2ProjectsResponse1`


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
from digitaloceanapi.models.v_2_projects_response_1 import V2ProjectsResponse1

v_2_projects_response_1 = V2ProjectsResponse1(
    project=Project(
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description4',
        environment=Environment.DEVELOPMENT,
        id='000026e4-0000-0000-0000-000000000000',
        name='name6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



