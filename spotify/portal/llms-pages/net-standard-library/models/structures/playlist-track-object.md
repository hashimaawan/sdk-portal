# Playlist Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tPYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`PlaylistTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddedAt` | `DateTime?` | Optional | The date and time the track or episode was added. _**Note**: some very old playlists may return `null` in this field._ |
| `AddedBy` | [`PlaylistUserObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/playlist-user-object.md) | Optional | The Spotify user who added the track or episode. _**Note**: some very old playlists may return `null` in this field._ |
| `IsLocal` | `bool?` | Optional | Whether this track or episode is a [local file](/documentation/web-api/concepts/playlists/#local-files) or not. |
| `Track` | [`PlaylistTrackObjectTrack`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/oneof-anyof-definitions/playlist-track-object-track.md) | Optional | This is a container for one-of cases. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models.Containers;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

PlaylistTrackObject playlistTrackObject = new PlaylistTrackObject
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
};
```



