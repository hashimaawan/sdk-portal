# Cursor Paging Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ09iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`CursorPagingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `str` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `limit` | `int` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `next` | `str` | Optional | URL to the next page of items. ( `null` if none) |
| `cursors` | [`CursorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `total` | `int` | Optional | The total number of items available to return. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.cursor_object import CursorObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.cursor_paging_object import CursorPagingObject

cursor_paging_object = CursorPagingObject(
    href='href0',
    limit=90,
    next='next4',
    cursors=CursorObject(
        after='after8',
        before='before6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    total=184,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



