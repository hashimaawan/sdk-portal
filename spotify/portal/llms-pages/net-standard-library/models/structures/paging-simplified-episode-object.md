# Paging Simplified Episode Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2luZ1NpbXBsaWZpZWRFcGlzb2RlT2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`PagingSimplifiedEpisodeObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `Limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `string` | Required | URL to the next page of items. ( `null` if none) |
| `Offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `Previous` | `string` | Required | URL to the previous page of items. ( `null` if none) |
| `Total` | `int` | Required | The total number of items available to return. |
| `Items` | [`List<EpisodeBase>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/episode-base.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

PagingSimplifiedEpisodeObject pagingSimplifiedEpisodeObject = new PagingSimplifiedEpisodeObject
{
    Href = "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
    Limit = 20,
    Next = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
    Offset = 0,
    Previous = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
    Total = 4,
    Items = new List<EpisodeBase>
    {
        new EpisodeBase
        {
            AudioPreviewUrl = "https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17",
            Description = "A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.\n",
            HtmlDescription = "<p>A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.</p>\n",
            DurationMs = 1686230,
            MExplicit = false,
            ExternalUrls = new ExternalUrlObject
            {
                Spotify = "spotify6",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Href = "https://api.spotify.com/v1/episodes/5Xt5DXGzch68nYYamXrNxZ",
            Id = "5Xt5DXGzch68nYYamXrNxZ",
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
            IsExternallyHosted = false,
            IsPlayable = false,
            Languages = new List<string>
            {
                "fr",
                "en",
            },
            Name = "Starting Your Own Podcast: Tips, Tricks, and Advice From Anchor Creators\n",
            ReleaseDate = "1981-12-15",
            ReleaseDatePrecision = ReleaseDatePrecision.Day,
            Type = "episode",
            Uri = "spotify:episode:0zLhl3WsOCQHbe1BPTiHgr",
            Language = "en",
            ResumePoint = new ResumePointObject
            {
                FullyPlayed = false,
                ResumePositionMs = 254,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Restrictions = new EpisodeRestrictionObject
            {
                Reason = "reason0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



