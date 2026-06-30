# Episode Base

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkVwaXNvZGVCYXNl

*This model accepts additional fields of type object.*


# Class Name

`EpisodeBase`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AudioPreviewUrl` | `string` | Required | A URL to a 30 second preview (MP3 format) of the episode. `null` if not available. |
| `Description` | `string` | Required | A description of the episode. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `HtmlDescription` | `string` | Required | A description of the episode. This field may contain HTML tags. |
| `DurationMs` | `int` | Required | The episode length in milliseconds. |
| `Explicit` | `bool` | Required | Whether or not the episode has explicit content (true = yes it does; false = no it does not OR unknown). |
| `ExternalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/external-url-object.md) | Required | External URLs for this episode. |
| `Href` | `string` | Required | A link to the Web API endpoint providing full details of the episode. |
| `Id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the episode. |
| `Images` | [`List<ImageObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/image-object.md) | Required | The cover art for the episode in various sizes, widest first. |
| `IsExternallyHosted` | `bool` | Required | True if the episode is hosted outside of Spotify's CDN. |
| `IsPlayable` | `bool` | Required | True if the episode is playable in the given market. Otherwise false. |
| `Language` | `string` | Optional | The language used in the episode, identified by a [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. This field is deprecated and might be removed in the future. Please use the `languages` field instead. |
| `Languages` | `List<string>` | Required | A list of the languages used in the episode, identified by their [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639) code. |
| `Name` | `string` | Required | The name of the episode. |
| `ReleaseDate` | `string` | Required | The date the episode was first released, for example `"1981-12-15"`. Depending on the precision, it might be shown as `"1981"` or `"1981-12"`. |
| `ReleaseDatePrecision` | [`ReleaseDatePrecision`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. |
| `ResumePoint` | [`ResumePointObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/resume-point-object.md) | Optional | The user's most recent position in the episode. Set if the supplied access token is a user token and has the scope 'user-read-playback-position'. |
| `Type` | `string` | Required, Constant | The object type.<br><br>**Value**: `"episode"` |
| `Uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the episode. |
| `Restrictions` | [`EpisodeRestrictionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/episode-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

EpisodeBase episodeBase = new EpisodeBase
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
};
```



