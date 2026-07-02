# Filter Definition

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkZpbHRlckRlZmluaXRpb24

A string for searching notebook names.

*This model accepts additional fields of type Any.*


# Class Name

`FilterDefinition`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.filter_definition import FilterDefinition

filter_definition = FilterDefinition(
    name='Name8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



