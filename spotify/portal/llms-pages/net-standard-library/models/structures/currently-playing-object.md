# Currently Playing Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdPYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`CurrentlyPlayingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Context` | [`ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. |
| `Timestamp` | `long?` | Optional | Unix Millisecond Timestamp when data was fetched |
| `ProgressMs` | `int?` | Optional | Progress into the currently playing track or episode. Can be `null`. |
| `IsPlaying` | `bool?` | Optional | If something is currently playing, return `true`. |
| `Item` | [`CurrentlyPlayingObjectItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/oneof-anyof-definitions/currently-playing-object-item.md) | Optional | This is a container for one-of cases. |
| `CurrentlyPlayingType` | `string` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. |
| `Actions` | [`DisallowsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models.Containers;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

CurrentlyPlayingObject currentlyPlayingObject = new CurrentlyPlayingObject
{
    Context = new ContextObject
    {
        Type = "type8",
        Href = "href4",
        ExternalUrls = new ExternalUrlObject
        {
            Spotify = "spotify6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Uri = "uri6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Timestamp = 254L,
    ProgressMs = 226,
    IsPlaying = false,
    Item = CurrentlyPlayingObjectItem.FromTrackObject(
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



