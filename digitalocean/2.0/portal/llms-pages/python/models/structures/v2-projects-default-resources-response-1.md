# V2 Projects Default Resources Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2ProjectsDefaultResourcesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resources` | [`List[Resources1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/resources-1.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.links_4 import Links4
from digitaloceanapi.models.resources_1 import Resources1
from digitaloceanapi.models.status_14 import Status14
from digitaloceanapi.models.v_2_projects_default_resources_response_1 import V2ProjectsDefaultResourcesResponse1

v_2_projects_default_resources_response_1 = V2ProjectsDefaultResourcesResponse1(
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
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



