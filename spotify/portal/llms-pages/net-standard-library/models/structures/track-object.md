# Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlRyYWNrT2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`TrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Album` | [`SimplifiedAlbumObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/simplified-album-object.md) | Optional | The album on which the track appears. The album object includes a link in `href` to full information about the album. |
| `Artists` | [`List<ArtistObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/artist-object.md) | Optional | The artists who performed the track. Each artist object includes a link in `href` to more detailed information about the artist. |
| `AvailableMarkets` | `List<string>` | Optional | A list of the countries in which the track can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `DiscNumber` | `int?` | Optional | The disc number (usually `1` unless the album consists of more than one disc). |
| `DurationMs` | `int?` | Optional | The track length in milliseconds. |
| `Explicit` | `bool?` | Optional | Whether or not the track has explicit lyrics ( `true` = yes it does; `false` = no it does not OR unknown). |
| `ExternalIds` | [`ExternalIdObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/external-id-object.md) | Optional | Known external IDs for the track. |
| `ExternalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/external-url-object.md) | Optional | Known external URLs for this track. |
| `Href` | `string` | Optional | A link to the Web API endpoint providing full details of the track. |
| `Id` | `string` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `IsPlayable` | `bool?` | Optional | Part of the response when [Track Relinking](/documentation/web-api/concepts/track-relinking) is applied. If `true`, the track is playable in the given market. Otherwise `false`. |
| `LinkedFrom` | [`LinkedTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/linked-track-object.md) | Optional | Part of the response when [Track Relinking](/documentation/web-api/concepts/track-relinking) is applied, and the requested track has been replaced with different track. The track in the `linked_from` object contains information about the originally requested track. |
| `Restrictions` | [`TrackRestrictionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/track-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `Name` | `string` | Optional | The name of the track. |
| `Popularity` | `int?` | Optional | The popularity of the track. The value will be between 0 and 100, with 100 being the most popular.<br/>The popularity of a track is a value between 0 and 100, with 100 being the most popular. The popularity is calculated by algorithm and is based, in the most part, on the total number of plays the track has had and how recent those plays are.<br/>Generally speaking, songs that are being played a lot now will have a higher popularity than songs that were played a lot in the past. Duplicate tracks (e.g. the same track from a single and an album) are rated independently. Artist and album popularity is derived mathematically from track popularity. _**Note**: the popularity value may lag actual popularity by a few days: the value is not updated in real time._ |
| `PreviewUrl` | `string` | Optional | A link to a 30 second preview (MP3 format) of the track. Can be `null` |
| `TrackNumber` | `int?` | Optional | The number of the track. If an album has several discs, the track number is the number on the specified disc. |
| `Type` | [`Type2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/enumerations/type-2.md) | Optional | The object type: "track". |
| `Uri` | `string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `IsLocal` | `bool?` | Optional | Whether or not the track is from a local file. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

TrackObject trackObject = new TrackObject
{
    Album = new SimplifiedAlbumObject
    {
        AlbumType = AlbumType.Single,
        TotalTracks = 170,
        AvailableMarkets = new List<string>
        {
            "available_markets2",
            "available_markets3",
        },
        ExternalUrls = new ExternalUrlObject
        {
            Spotify = "spotify6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Href = "href0",
        Id = "id8",
        Images = new List<ImageObject>
        {
            new ImageObject
            {
                Url = "url6",
                Height = 182,
                Width = 222,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Name = "name8",
        ReleaseDate = "release_date6",
        ReleaseDatePrecision = ReleaseDatePrecision.Day,
        Type = "type2",
        Uri = "uri2",
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
    },
    Artists = new List<ArtistObject>
    {
        new ArtistObject
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
            Genres = new List<string>
            {
                "genres7",
                "genres8",
            },
            Href = "href2",
            Id = "id0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new ArtistObject
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
            Genres = new List<string>
            {
                "genres7",
                "genres8",
            },
            Href = "href2",
            Id = "id0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    AvailableMarkets = new List<string>
    {
        "available_markets2",
        "available_markets3",
        "available_markets4",
    },
    DiscNumber = 182,
    DurationMs = 246,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



