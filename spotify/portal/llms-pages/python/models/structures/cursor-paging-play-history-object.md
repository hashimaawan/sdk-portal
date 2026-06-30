# Cursor Paging Play History Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ1BsYXlIaXN0b3J5T2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`CursorPagingPlayHistoryObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `str` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `limit` | `int` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `next` | `str` | Optional | URL to the next page of items. ( `null` if none) |
| `cursors` | [`CursorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `total` | `int` | Optional | The total number of items available to return. |
| `items` | [`List[PlayHistoryObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/play-history-object.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.cursor_object import CursorObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.cursor_paging_play_history_object import CursorPagingPlayHistoryObject

cursor_paging_play_history_object = CursorPagingPlayHistoryObject(
    href='href0',
    limit=234,
    next='next6',
    cursors=CursorObject(
        after='after8',
        before='before6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    total=72,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



