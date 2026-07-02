# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_arn` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tag_keys` | `List[str]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```python
from amazonathena.models.untag_resource_input import UntagResourceInput

untag_resource_input = UntagResourceInput(
    resource_arn='ResourceARN4',
    tag_keys=[
        'TagKeys9'
    ]
)
```



