# Search Items

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlNlYXJjaEl0ZW1z

*This model accepts additional fields of type object.*


# Class Name

`SearchItems`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tracks` | [`PagingTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/paging-track-object.md) | Optional | - |
| `Artists` | [`PagingArtistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/paging-artist-object.md) | Optional | - |
| `Albums` | [`PagingSimplifiedAlbumObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/paging-simplified-album-object.md) | Optional | - |
| `Playlists` | [`PagingPlaylistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/paging-playlist-object.md) | Optional | - |
| `Shows` | [`PagingSimplifiedShowObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/paging-simplified-show-object.md) | Optional | - |
| `Episodes` | [`PagingSimplifiedEpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/paging-simplified-episode-object.md) | Optional | - |
| `Audiobooks` | [`PagingSimplifiedAudiobookObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/paging-simplified-audiobook-object.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

SearchItems searchItems = new SearchItems
{
    Tracks = new PagingTrackObject
    {
        Href = "href6",
        Limit = 142,
        Next = "next8",
        Offset = 238,
        Previous = "previous2",
        Total = 236,
        Items = new List<TrackObject>
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
                },
                AvailableMarkets = new List<string>
                {
                    "available_markets2",
                },
                DiscNumber = 244,
                DurationMs = 52,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Artists = new PagingArtistObject
    {
        Href = "href2",
        Limit = 214,
        Next = "next2",
        Offset = 54,
        Previous = "previous8",
        Total = 52,
        Items = new List<ArtistObject>
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
                    "genres5",
                    "genres6",
                },
                Href = "href0",
                Id = "id8",
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
                    "genres5",
                    "genres6",
                },
                Href = "href0",
                Id = "id8",
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
                    "genres5",
                    "genres6",
                },
                Href = "href0",
                Id = "id8",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Albums = new PagingSimplifiedAlbumObject
    {
        Href = "href0",
        Limit = 0,
        Next = "next4",
        Offset = 96,
        Previous = "previous6",
        Total = 94,
        Items = new List<SimplifiedAlbumObject>
        {
            new SimplifiedAlbumObject
            {
                AlbumType = AlbumType.Album,
                TotalTracks = 196,
                AvailableMarkets = new List<string>
                {
                    "available_markets2",
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
                ReleaseDatePrecision = ReleaseDatePrecision.Month,
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
                },
                Restrictions = new AlbumRestrictionObject
                {
                    Reason = Reason.Explicit,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Playlists = new PagingPlaylistObject
    {
        Href = "href2",
        Limit = 68,
        Next = "next2",
        Offset = 164,
        Previous = "previous8",
        Total = 162,
        Items = new List<SimplifiedPlaylistObject>
        {
            new SimplifiedPlaylistObject
            {
                Collaborative = false,
                Description = "description2",
                ExternalUrls = new ExternalUrlObject
                {
                    Spotify = "spotify6",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Href = "href0",
                Id = "id8",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new SimplifiedPlaylistObject
            {
                Collaborative = false,
                Description = "description2",
                ExternalUrls = new ExternalUrlObject
                {
                    Spotify = "spotify6",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Href = "href0",
                Id = "id8",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new SimplifiedPlaylistObject
            {
                Collaborative = false,
                Description = "description2",
                ExternalUrls = new ExternalUrlObject
                {
                    Spotify = "spotify6",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Href = "href0",
                Id = "id8",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Shows = new PagingSimplifiedShowObject
    {
        Href = "href0",
        Limit = 248,
        Next = "next6",
        Offset = 88,
        Previous = "previous6",
        Total = 86,
        Items = new List<ShowBase>
        {
            new ShowBase
            {
                AvailableMarkets = new List<string>
                {
                    "available_markets2",
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
                Description = "description2",
                HtmlDescription = "html_description2",
                MExplicit = false,
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
                    new ImageObject
                    {
                        Url = "url6",
                        Height = 182,
                        Width = 222,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                IsExternallyHosted = false,
                Languages = new List<string>
                {
                    "languages5",
                },
                MediaType = "media_type4",
                Name = "name8",
                Publisher = "publisher4",
                Type = "type2",
                Uri = "uri2",
                TotalEpisodes = 166,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new ShowBase
            {
                AvailableMarkets = new List<string>
                {
                    "available_markets2",
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
                Description = "description2",
                HtmlDescription = "html_description2",
                MExplicit = false,
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
                    new ImageObject
                    {
                        Url = "url6",
                        Height = 182,
                        Width = 222,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                IsExternallyHosted = false,
                Languages = new List<string>
                {
                    "languages5",
                },
                MediaType = "media_type4",
                Name = "name8",
                Publisher = "publisher4",
                Type = "type2",
                Uri = "uri2",
                TotalEpisodes = 166,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new ShowBase
            {
                AvailableMarkets = new List<string>
                {
                    "available_markets2",
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
                Description = "description2",
                HtmlDescription = "html_description2",
                MExplicit = false,
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
                    new ImageObject
                    {
                        Url = "url6",
                        Height = 182,
                        Width = 222,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                IsExternallyHosted = false,
                Languages = new List<string>
                {
                    "languages5",
                },
                MediaType = "media_type4",
                Name = "name8",
                Publisher = "publisher4",
                Type = "type2",
                Uri = "uri2",
                TotalEpisodes = 166,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



