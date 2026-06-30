# Saved Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlNhdmVkQWxidW1PYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`SavedAlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddedAt` | `DateTime?` | Optional | The date and time the album was saved<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `Album` | [`AlbumObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/album-object.md) | Optional | Information about the album. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

SavedAlbumObject savedAlbumObject = new SavedAlbumObject
{
    AddedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Album = new AlbumObject
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
        Tracks = new PagingSimplifiedTrackObject
        {
            Href = "href6",
            Limit = 142,
            Next = "next8",
            Offset = 238,
            Previous = "previous2",
            Total = 236,
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
            "genres5",
            "genres6",
            "genres7",
        },
        Label = "label8",
        Popularity = 78,
        Restrictions = new AlbumRestrictionObject
        {
            Reason = Reason.Explicit,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



