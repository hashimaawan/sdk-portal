# Delete Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRlbGV0ZVdvcmtHcm91cElucHV0


# Class Name

`DeleteWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `recursive_delete_option` | `bool` | Optional | - |


# Example

```python
from amazonathena.models.delete_work_group_input import DeleteWorkGroupInput

delete_work_group_input = DeleteWorkGroupInput(
    work_group='WorkGroup8',
    recursive_delete_option=False
)
```



