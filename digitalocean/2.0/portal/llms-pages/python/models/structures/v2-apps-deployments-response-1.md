# V2 Apps Deployments Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBEZXBsb3ltZW50cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsDeploymentsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deployment` | [`AnAppDeployment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/an-app-deployment.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.an_app_deployment import AnAppDeployment
from digitaloceanapi.models.functions_components_that_are_part_of_this_deployment import FunctionsComponentsThatArePartOfThisDeployment
from digitaloceanapi.models.v_2_apps_deployments_response_1 import V2AppsDeploymentsResponse1

v_2_apps_deployments_response_1 = V2AppsDeploymentsResponse1(
    deployment=AnAppDeployment(
        cause='cause8',
        cloned_from='cloned_from0',
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        functions=[
            FunctionsComponentsThatArePartOfThisDeployment(
                name='name4',
                namespace='namespace8',
                source_commit_hash='source_commit_hash4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        id='id2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



