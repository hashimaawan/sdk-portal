# Playlists Tracks Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwVHJhY2tzJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type Any.*


# Class Name

`PlaylistsTracksRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tracks` | [`List[Track1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/track-1.md) | Required | An array of objects containing [Spotify URIs](/documentation/web-api/concepts/spotify-uris-ids) of the tracks or episodes to remove.<br>For example: `{ "tracks": [{ "uri": "spotify:track:4iV5W9uYEdYUVa79Axb7Rh" },{ "uri": "spotify:track:1301WleyT98MSxVHPZCA6M" }] }`. A maximum of 100 objects can be sent at once. |
| `snapshot_id` | `str` | Optional | The playlist's snapshot ID against which you want to make the changes.<br>The API will validate that the specified items exist and in the specified positions and make the changes,<br>even if more recent changes have been made to the playlist. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.playlists_tracks_request_2 import PlaylistsTracksRequest2
from spotifywebapiwithfixesandimprovementsfromsonallux.models.track_1 import Track1

playlists_tracks_request_2 = PlaylistsTracksRequest2(
    tracks=[
        Track1(
            uri='uri8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    snapshot_id='snapshot_id4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



