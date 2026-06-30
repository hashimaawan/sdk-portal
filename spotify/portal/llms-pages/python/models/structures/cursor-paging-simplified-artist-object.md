# Cursor Paging Simplified Artist Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ1NpbXBsaWZpZWRBcnRpc3RPYmplY3Q

*This model accepts additional fields of type Any.*


# Class Name

`CursorPagingSimplifiedArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `str` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `limit` | `int` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `next` | `str` | Optional | URL to the next page of items. ( `null` if none) |
| `cursors` | [`CursorObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `total` | `int` | Optional | The total number of items available to return. |
| `items` | [`List[ArtistObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/artist-object.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.cursor_object import CursorObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.cursor_paging_simplified_artist_object import CursorPagingSimplifiedArtistObject

cursor_paging_simplified_artist_object = CursorPagingSimplifiedArtistObject(
    href='href8',
    limit=172,
    next='next4',
    cursors=CursorObject(
        after='after8',
        before='before6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    total=10,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



