# V2 Tags Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNvdXJjZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2TagsResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resources` | [`List[Resources3]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/resources-3.md) | Required | An array of objects containing resource_id and resource_type  attributes. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.resource_type_2 import ResourceType2
from digitaloceanapi.models.resources_3 import Resources3
from digitaloceanapi.models.v_2_tags_resources_request import V2TagsResourcesRequest

v_2_tags_resources_request = V2TagsResourcesRequest(
    resources=[
        Resources3(
            resource_id='9569411',
            resource_type=ResourceType2.DROPLET,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Resources3(
            resource_id='7555620',
            resource_type=ResourceType2.IMAGE,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Resources3(
            resource_id='3d80cb72-342b-4aaa-b92e-4e4abb24a933',
            resource_type=ResourceType2.VOLUME,
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



