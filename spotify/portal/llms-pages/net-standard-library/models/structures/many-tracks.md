# Many Tracks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1hbnlUcmFja3M

*This model accepts additional fields of type object.*


# Class Name

`ManyTracks`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tracks` | [`List<TrackObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/track-object.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

ManyTracks manyTracks = new ManyTracks
{
    Tracks = new List<TrackObject>
    {
        new TrackObject
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
                "available_markets8",
                "available_markets9",
            },
            DiscNumber = 168,
            DurationMs = 232,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



