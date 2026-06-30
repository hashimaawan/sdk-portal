# Playlist Tracks Ref Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tzUmVmT2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`PlaylistTracksRefObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Optional | A link to the Web API endpoint where full details of the playlist's tracks can be retrieved. |
| `Total` | `int?` | Optional | Number of tracks in the playlist. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

PlaylistTracksRefObject playlistTracksRefObject = new PlaylistTracksRefObject
{
    Href = "href6",
    Total = 80,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



