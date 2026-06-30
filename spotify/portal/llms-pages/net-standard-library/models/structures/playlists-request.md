# Playlists Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type object.*


# Class Name

`PlaylistsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Optional | The new name for the playlist, for example `"My New Playlist Title"` |
| `Public` | `bool?` | Optional | If `true` the playlist will be public, if `false` it will be private. |
| `Collaborative` | `bool?` | Optional | If `true`, the playlist will become collaborative and other users will be able to modify the playlist in their Spotify client. <br/><br>_**Note**: You can only set `collaborative` to `true` on non-public playlists._ |
| `Description` | `string` | Optional | Value for playlist description as displayed in Spotify Clients and in the Web API. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

PlaylistsRequest playlistsRequest = new PlaylistsRequest
{
    Name = "Updated Playlist Name",
    MPublic = false,
    Collaborative = false,
    Description = "Updated playlist description",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



