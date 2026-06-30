# Playlists Followers Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwRm9sbG93ZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`PlaylistsFollowersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `public` | `bool` | Optional | Defaults to `true`. If `true` the playlist will be included in user's public playlists, if `false` it will remain private. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.playlists_followers_request import PlaylistsFollowersRequest

playlists_followers_request = PlaylistsFollowersRequest(
    public=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



