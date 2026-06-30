# Cursor Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRkN1cnNvck9iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`CursorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `after` | `str` | Optional | The cursor to use as key to find the next page of items. |
| `before` | `str` | Optional | The cursor to use as key to find the previous page of items. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.cursor_object import CursorObject

cursor_object = CursorObject(
    after='after8',
    before='before6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



