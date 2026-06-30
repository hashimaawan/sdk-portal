# Paging Playlist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRlBhZ2luZ1BsYXlsaXN0T2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`PagingPlaylistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `str` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `next` | `str` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `str` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `int` | Required | The total number of items available to return. |
| `items` | [`List[SimplifiedPlaylistObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/simplified-playlist-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_playlist_object import PagingPlaylistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_playlist_object import SimplifiedPlaylistObject

paging_playlist_object = PagingPlaylistObject(
    href='https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
    limit=20,
    next='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    offset=0,
    previous='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    total=4,
    items=[
        SimplifiedPlaylistObject(
            collaborative=False,
            description='description2',
            external_urls=ExternalUrlObject(
                spotify='spotify6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            href='href0',
            id='id8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



