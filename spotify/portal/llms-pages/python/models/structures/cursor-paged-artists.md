# Cursor Paged Artists

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRkN1cnNvclBhZ2VkQXJ0aXN0cw

*This model accepts additional fields of type Any.*


# Class Name

`CursorPagedArtists`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `artists` | [`CursorPagingSimplifiedArtistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/cursor-paging-simplified-artist-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.cursor_object import CursorObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.cursor_paged_artists import CursorPagedArtists
from spotifywebapiwithfixesandimprovementsfromsonallux.models.cursor_paging_simplified_artist_object import CursorPagingSimplifiedArtistObject

cursor_paged_artists = CursorPagedArtists(
    artists=CursorPagingSimplifiedArtistObject(
        href='href2',
        limit=214,
        next='next2',
        cursors=CursorObject(
            after='after8',
            before='before6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        total=52,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



