# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_arn` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tag_keys` | `List[str]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.untag_resource_input import UntagResourceInput

untag_resource_input = UntagResourceInput(
    resource_arn='ResourceARN4',
    tag_keys=[
        'TagKeys9'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



