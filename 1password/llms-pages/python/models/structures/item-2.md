# Item 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRkl0ZW0y

*This model accepts additional fields of type Any.*


# Class Name

`Item2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.item_2 import Item2

item_2 = Item2(
    id='id0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



