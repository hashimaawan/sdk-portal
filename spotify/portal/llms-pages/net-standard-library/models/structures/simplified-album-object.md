# Simplified Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRBbGJ1bU9iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`SimplifiedAlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AlbumType` | [`AlbumType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/enumerations/album-type.md) | Required | The type of the album. |
| `TotalTracks` | `int` | Required | The number of tracks in the album. |
| `AvailableMarkets` | `List<string>` | Required | The markets in which the album is available: [ISO 3166-1 alpha-2 country codes](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _**NOTE**: an album is considered available in a market when at least 1 of its tracks is available in that market._ |
| `ExternalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/external-url-object.md) | Required | Known external URLs for this album. |
| `Href` | `string` | Required | A link to the Web API endpoint providing full details of the album. |
| `Id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `Images` | [`List<ImageObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/image-object.md) | Required | The cover art for the album in various sizes, widest first. |
| `Name` | `string` | Required | The name of the album. In case of an album takedown, the value may be an empty string. |
| `ReleaseDate` | `string` | Required | The date the album was first released. |
| `ReleaseDatePrecision` | [`ReleaseDatePrecision`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. |
| `Restrictions` | [`AlbumRestrictionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/album-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `Type` | `string` | Required, Constant | The object type.<br><br>**Value**: `"album"` |
| `Uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `Artists` | [`List<SimplifiedArtistObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/simplified-artist-object.md) | Required | The artists of the album. Each artist object includes a link in `href` to more detailed information about the artist. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

SimplifiedAlbumObject simplifiedAlbumObject = new SimplifiedAlbumObject
{
    AlbumType = AlbumType.Compilation,
    TotalTracks = 9,
    AvailableMarkets = new List<string>
    {
        "CA",
        "BR",
        "IT",
    },
    ExternalUrls = new ExternalUrlObject
    {
        Spotify = "spotify6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Href = "href4",
    Id = "2up3OPMp9Tb4dAKM2erWXQ",
    Images = new List<ImageObject>
    {
        new ImageObject
        {
            Url = "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
            Height = 300,
            Width = 300,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Name = "name2",
    ReleaseDate = "1981-12",
    ReleaseDatePrecision = ReleaseDatePrecision.Year,
    Type = "album",
    Uri = "spotify:album:2up3OPMp9Tb4dAKM2erWXQ",
    Artists = new List<SimplifiedArtistObject>
    {
        new SimplifiedArtistObject
        {
            ExternalUrls = new ExternalUrlObject
            {
                Spotify = "spotify6",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Href = "href2",
            Id = "id0",
            Name = "name0",
            Type = SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models.Type.Artist,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Restrictions = new AlbumRestrictionObject
    {
        Reason = Reason.Explicit,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



