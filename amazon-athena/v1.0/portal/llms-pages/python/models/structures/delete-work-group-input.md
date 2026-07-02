# Delete Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRlbGV0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type Any.*


# Class Name

`DeleteWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `recursive_delete_option` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.delete_work_group_input import DeleteWorkGroupInput

delete_work_group_input = DeleteWorkGroupInput(
    work_group='WorkGroup8',
    recursive_delete_option=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



