# Users Playlists Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlVzZXJzJTI1MjBQbGF5bGlzdHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`UsersPlaylistsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | The name for the new playlist, for example `"Your Coolest Playlist"`. This name does not need to be unique; a user may have several playlists with the same name. |
| `public` | `bool` | Optional | Defaults to `true`. If `true` the playlist will be public, if `false` it will be private. To be able to create private playlists, the user must have granted the `playlist-modify-private` [scope](/documentation/web-api/concepts/scopes/#list-of-scopes) |
| `collaborative` | `bool` | Optional | Defaults to `false`. If `true` the playlist will be collaborative. _**Note**: to create a collaborative playlist you must also set `public` to `false`. To create collaborative playlists you must have granted `playlist-modify-private` and `playlist-modify-public` [scopes](/documentation/web-api/concepts/scopes/#list-of-scopes)._ |
| `description` | `str` | Optional | value for playlist description as displayed in Spotify Clients and in the Web API. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.users_playlists_request import UsersPlaylistsRequest

users_playlists_request = UsersPlaylistsRequest(
    name='New Playlist',
    public=False,
    collaborative=False,
    description='New playlist description',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



