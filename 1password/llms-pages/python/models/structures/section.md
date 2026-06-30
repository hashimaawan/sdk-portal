# Section

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRlNlY3Rpb24

*This model accepts additional fields of type Any.*


# Class Name

`Section`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.section import Section

section = Section(
    id='id6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



