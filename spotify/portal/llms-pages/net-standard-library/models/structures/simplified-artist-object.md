# Simplified Artist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRBcnRpc3RPYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`SimplifiedArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/external-url-object.md) | Optional | Known external URLs for this artist. |
| `Href` | `string` | Optional | A link to the Web API endpoint providing full details of the artist. |
| `Id` | `string` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `Name` | `string` | Optional | The name of the artist. |
| `Type` | [`Type?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/enumerations/type.md) | Optional | The object type. |
| `Uri` | `string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

SimplifiedArtistObject simplifiedArtistObject = new SimplifiedArtistObject
{
    ExternalUrls = new ExternalUrlObject
    {
        Spotify = "spotify6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Href = "href6",
    Id = "id4",
    Name = "name4",
    Type = SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models.Type.Artist,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



