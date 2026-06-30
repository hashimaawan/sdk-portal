# Queue Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXVlT2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`QueueObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CurrentlyPlaying` | [`QueueObjectCurrentlyPlaying`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/oneof-anyof-definitions/queue-object-currently-playing.md) | Optional | This is a container for one-of cases. |
| `Queue` | [`List<QueueObjectQueue>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/oneof-anyof-definitions/queue-object-queue.md) | Optional | This is List of a container for one-of cases. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models.Containers;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

QueueObject queueObject = new QueueObject
{
    CurrentlyPlaying = QueueObjectCurrentlyPlaying.FromTrackObject(
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
            },
            AvailableMarkets = new List<string>
            {
                "available_markets6",
                "available_markets7",
            },
            DiscNumber = 30,
            DurationMs = 222,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        }
    ),
    Queue = new List<QueueObjectQueue>
    {
        QueueObjectQueue.FromTrackObject(
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
                },
                AvailableMarkets = new List<string>
                {
                    "available_markets6",
                    "available_markets7",
                },
                DiscNumber = 30,
                DurationMs = 222,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
        QueueObjectQueue.FromTrackObject(
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
                },
                AvailableMarkets = new List<string>
                {
                    "available_markets6",
                    "available_markets7",
                },
                DiscNumber = 30,
                DurationMs = 222,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
        QueueObjectQueue.FromTrackObject(
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
                },
                AvailableMarkets = new List<string>
                {
                    "available_markets6",
                    "available_markets7",
                },
                DiscNumber = 30,
                DurationMs = 222,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



