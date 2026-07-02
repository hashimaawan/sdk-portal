# Tag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlRhZ1Jlc291cmNlSW5wdXQ


# Class Name

`TagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_arn` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tags` | [`List[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/tag.md) | Required | - |


# Example

```python
from amazonathena.models.tag import Tag
from amazonathena.models.tag_resource_input import TagResourceInput

tag_resource_input = TagResourceInput(
    resource_arn='ResourceARN0',
    tags=[
        Tag(
            key='Key0',
            value='Value6'
        )
    ]
)
```



