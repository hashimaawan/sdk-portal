# Playlist User Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlBsYXlsaXN0VXNlck9iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`PlaylistUserObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/external-url-object.md) | Optional | Known public external URLs for this user. |
| `Followers` | [`FollowersObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/followers-object.md) | Optional | Information about the followers of this user. |
| `Href` | `string` | Optional | A link to the Web API endpoint for this user. |
| `Id` | `string` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `Type` | [`Type3?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/enumerations/type-3.md) | Optional | The object type. |
| `Uri` | `string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

PlaylistUserObject playlistUserObject = new PlaylistUserObject
{
    ExternalUrls = new ExternalUrlObject
    {
        Spotify = "spotify6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Followers = new FollowersObject
    {
        Href = "href0",
        Total = 82,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Href = "href0",
    Id = "id8",
    Type = Type3.User,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



