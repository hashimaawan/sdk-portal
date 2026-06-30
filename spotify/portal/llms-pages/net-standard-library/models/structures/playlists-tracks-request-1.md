# Playlists Tracks Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwVHJhY2tzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type object.*


# Class Name

`PlaylistsTracksRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Uris` | `List<string>` | Optional | - |
| `RangeStart` | `int?` | Optional | The position of the first item to be reordered. |
| `InsertBefore` | `int?` | Optional | The position where the items should be inserted.<br/>To reorder the items to the end of the playlist, simply set _insert_before_ to the position after the last item.<br/>Examples:<br/>To reorder the first item to the last position in a playlist with 10 items, set _range_start_ to 0, and _insert_before_ to 10.<br/>To reorder the last item in a playlist with 10 items to the start of the playlist, set _range_start_ to 9, and _insert_before_ to 0. |
| `RangeLength` | `int?` | Optional | The amount of items to be reordered. Defaults to 1 if not set.<br/>The range of items to be reordered begins from the _range_start_ position, and includes the _range_length_ subsequent items.<br/>Example:<br/>To move the items at index 9-10 to the start of the playlist, _range_start_ is set to 9, and _range_length_ is set to 2. |
| `SnapshotId` | `string` | Optional | The playlist's snapshot ID against which you want to make the changes. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

PlaylistsTracksRequest1 playlistsTracksRequest1 = new PlaylistsTracksRequest1
{
    Uris = new List<string>
    {
        "uris9",
    },
    RangeStart = 1,
    InsertBefore = 3,
    RangeLength = 2,
    SnapshotId = "snapshot_id4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



