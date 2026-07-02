# Column

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNvbHVtbg

Contains metadata for a column in a table.

*This model accepts additional fields of type Any.*


# Class Name

`Column`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `mtype` | `str` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096` |
| `comment` | `str` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `255` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.column import Column

column = Column(
    name='Name6',
    mtype='Type6',
    comment='Comment2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



