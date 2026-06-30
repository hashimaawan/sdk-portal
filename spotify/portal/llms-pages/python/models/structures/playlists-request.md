# Playlists Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`PlaylistsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | The new name for the playlist, for example `"My New Playlist Title"` |
| `public` | `bool` | Optional | If `true` the playlist will be public, if `false` it will be private. |
| `collaborative` | `bool` | Optional | If `true`, the playlist will become collaborative and other users will be able to modify the playlist in their Spotify client. <br/><br>_**Note**: You can only set `collaborative` to `true` on non-public playlists._ |
| `description` | `str` | Optional | Value for playlist description as displayed in Spotify Clients and in the Web API. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.playlists_request import PlaylistsRequest

playlists_request = PlaylistsRequest(
    name='Updated Playlist Name',
    public=False,
    collaborative=False,
    description='Updated playlist description',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



