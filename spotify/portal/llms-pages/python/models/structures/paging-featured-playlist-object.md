# Paging Featured Playlist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlBhZ2luZ0ZlYXR1cmVkUGxheWxpc3RPYmplY3Q

*This model accepts additional fields of type Any.*


# Class Name

`PagingFeaturedPlaylistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `str` | Optional | The localized message of a playlist. |
| `playlists` | [`PagingPlaylistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/paging-playlist-object.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_featured_playlist_object import PagingFeaturedPlaylistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_playlist_object import PagingPlaylistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_playlist_object import SimplifiedPlaylistObject

paging_featured_playlist_object = PagingFeaturedPlaylistObject(
    message='Popular Playlists',
    playlists=PagingPlaylistObject(
        href='href2',
        limit=68,
        next='next2',
        offset=164,
        previous='previous8',
        total=162,
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
            ),
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
            ),
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
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



