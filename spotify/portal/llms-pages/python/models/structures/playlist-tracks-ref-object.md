# Playlist Tracks Ref Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tzUmVmT2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`PlaylistTracksRefObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `str` | Optional | A link to the Web API endpoint where full details of the playlist's tracks can be retrieved. |
| `total` | `int` | Optional | Number of tracks in the playlist. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.playlist_tracks_ref_object import PlaylistTracksRefObject

playlist_tracks_ref_object = PlaylistTracksRefObject(
    href='href8',
    total=22,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



