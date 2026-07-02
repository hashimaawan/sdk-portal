# List Work Groups Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzSW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ListWorkGroupsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_work_groups_input import ListWorkGroupsInput

list_work_groups_input = ListWorkGroupsInput(
    next_token='NextToken8',
    max_results=50,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



