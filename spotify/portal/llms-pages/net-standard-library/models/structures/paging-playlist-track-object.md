# Paging Playlist Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2luZ1BsYXlsaXN0VHJhY2tPYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`PagingPlaylistTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `Limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `string` | Required | URL to the next page of items. ( `null` if none) |
| `Offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `Previous` | `string` | Required | URL to the previous page of items. ( `null` if none) |
| `Total` | `int` | Required | The total number of items available to return. |
| `Items` | [`List<PlaylistTrackObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/playlist-track-object.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models.Containers;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

PagingPlaylistTrackObject pagingPlaylistTrackObject = new PagingPlaylistTrackObject
{
    Href = "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
    Limit = 20,
    Next = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
    Offset = 0,
    Previous = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
    Total = 4,
    Items = new List<PlaylistTrackObject>
    {
        new PlaylistTrackObject
        {
            AddedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            AddedBy = new PlaylistUserObject
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
                Href = "href6",
                Id = "id4",
                Type = Type3.User,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            IsLocal = false,
            Track = PlaylistTrackObjectTrack.FromTrackObject(
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



