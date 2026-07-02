# List Tags for Resource Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VPdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ListTagsForResourceOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tags` | [`List[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/tag.md) | Optional | - |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_tags_for_resource_output import ListTagsForResourceOutput
from amazonathena.models.tag import Tag

list_tags_for_resource_output = ListTagsForResourceOutput(
    tags=[
        Tag(
            key='Key0',
            value='Value6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    next_token='NextToken4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



