# Playlists Followers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwRm9sbG93ZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type object.*


# Class Name

`PlaylistsFollowersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Public` | `bool?` | Optional | Defaults to `true`. If `true` the playlist will be included in user's public playlists, if `false` it will remain private. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

PlaylistsFollowersRequest playlistsFollowersRequest = new PlaylistsFollowersRequest
{
    MPublic = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



