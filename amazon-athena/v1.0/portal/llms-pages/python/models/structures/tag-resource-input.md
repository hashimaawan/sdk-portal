# Tag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlRhZ1Jlc291cmNlSW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`TagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_arn` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tags` | [`List[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/tag.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.tag import Tag
from amazonathena.models.tag_resource_input import TagResourceInput

tag_resource_input = TagResourceInput(
    resource_arn='ResourceARN0',
    tags=[
        Tag(
            key='Key0',
            value='Value6',
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



