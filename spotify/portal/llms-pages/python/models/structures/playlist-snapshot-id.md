# Playlist Snapshot Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRlBsYXlsaXN0U25hcHNob3RJZA

*This model accepts additional fields of type Any.*


# Class Name

`PlaylistSnapshotId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshot_id` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.playlist_snapshot_id import PlaylistSnapshotId

playlist_snapshot_id = PlaylistSnapshotId(
    snapshot_id='abc',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



