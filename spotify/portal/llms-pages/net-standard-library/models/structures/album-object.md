# Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFsYnVtT2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`AlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AlbumType` | [`AlbumType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/enumerations/album-type.md) | Required | The type of the album. |
| `TotalTracks` | `int` | Required | The number of tracks in the album. |
| `AvailableMarkets` | `List<string>` | Required | The markets in which the album is available: [ISO 3166-1 alpha-2 country codes](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _**NOTE**: an album is considered available in a market when at least 1 of its tracks is available in that market._ |
| `ExternalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/external-url-object.md) | Required | Known external URLs for this album. |
| `Href` | `string` | Required | A link to the Web API endpoint providing full details of the album. |
| `Id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `Images` | [`List<ImageObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/image-object.md) | Required | The cover art for the album in various sizes, widest first. |
| `Name` | `string` | Required | The name of the album. In case of an album takedown, the value may be an empty string. |
| `ReleaseDate` | `string` | Required | The date the album was first released. |
| `ReleaseDatePrecision` | [`ReleaseDatePrecision`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. |
| `Restrictions` | [`AlbumRestrictionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/album-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `Type` | `string` | Required, Constant | The object type.<br><br>**Value**: `"album"` |
| `Uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `Artists` | [`List<SimplifiedArtistObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/simplified-artist-object.md) | Required | The artists of the album. Each artist object includes a link in `href` to more detailed information about the artist. |
| `Tracks` | [`PagingSimplifiedTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/paging-simplified-track-object.md) | Required | The tracks of the album. |
| `Copyrights` | [`List<CopyrightObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/copyright-object.md) | Required | The copyright statements of the album. |
| `ExternalIds` | [`ExternalIdObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/external-id-object.md) | Required | Known external IDs for the album. |
| `Genres` | `List<string>` | Required | A list of the genres the album is associated with. If not yet classified, the array is empty. |
| `Label` | `string` | Required | The label associated with the album. |
| `Popularity` | `int` | Required | The popularity of the album. The value will be between 0 and 100, with 100 being the most popular. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

AlbumObject albumObject = new AlbumObject
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
    Href = "href8",
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
    Name = "name6",
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
    Tracks = new PagingSimplifiedTrackObject
    {
        Href = "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
        Limit = 20,
        Next = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
        Offset = 0,
        Previous = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
        Total = 4,
        Items = new List<SimplifiedTrackObject>
        {
            new SimplifiedTrackObject
            {
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
                AvailableMarkets = new List<string>
                {
                    "available_markets2",
                },
                DiscNumber = 244,
                DurationMs = 52,
                MExplicit = false,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Copyrights = new List<CopyrightObject>
    {
        new CopyrightObject
        {
            Text = "text2",
            Type = "type2",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ExternalIds = new ExternalIdObject
    {
        Isrc = "isrc8",
        Ean = "ean8",
        Upc = "upc2",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Genres = new List<string>
    {
        "Egg punk",
        "Noise rock",
    },
    Label = "label6",
    Popularity = 152,
    Restrictions = new AlbumRestrictionObject
    {
        Reason = Reason.Explicit,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



