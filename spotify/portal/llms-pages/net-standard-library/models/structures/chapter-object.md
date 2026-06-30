# Chapter Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkNoYXB0ZXJPYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`ChapterObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AudioPreviewUrl` | `string` | Required | A URL to a 30 second preview (MP3 format) of the chapter. `null` if not available. |
| `AvailableMarkets` | `List<string>` | Optional | A list of the countries in which the chapter can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `ChapterNumber` | `int` | Required | The number of the chapter |
| `Description` | `string` | Required | A description of the chapter. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `HtmlDescription` | `string` | Required | A description of the chapter. This field may contain HTML tags. |
| `DurationMs` | `int` | Required | The chapter length in milliseconds. |
| `Explicit` | `bool` | Required | Whether or not the chapter has explicit content (true = yes it does; false = no it does not OR unknown). |
| `ExternalUrls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/external-url-object.md) | Required | External URLs for this chapter. |
| `Href` | `string` | Required | A link to the Web API endpoint providing full details of the chapter. |
| `Id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the chapter. |
| `Images` | [`List<ImageObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/image-object.md) | Required | The cover art for the chapter in various sizes, widest first. |
| `IsPlayable` | `bool` | Required | True if the chapter is playable in the given market. Otherwise false. |
| `Languages` | `List<string>` | Required | A list of the languages used in the chapter, identified by their [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639) code. |
| `Name` | `string` | Required | The name of the chapter. |
| `ReleaseDate` | `string` | Required | The date the chapter was first released, for example `"1981-12-15"`. Depending on the precision, it might be shown as `"1981"` or `"1981-12"`. |
| `ReleaseDatePrecision` | [`ReleaseDatePrecision`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. |
| `ResumePoint` | [`ResumePointObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/resume-point-object.md) | Optional | The user's most recent position in the chapter. Set if the supplied access token is a user token and has the scope 'user-read-playback-position'. |
| `Type` | `string` | Required, Constant | The object type.<br><br>**Value**: `"episode"` |
| `Uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the chapter. |
| `Restrictions` | [`ChapterRestrictionObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/chapter-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `Audiobook` | [`AudiobookBase`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/audiobook-base.md) | Required | The audiobook for which the chapter belongs. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

ChapterObject chapterObject = new ChapterObject
{
    AudioPreviewUrl = "https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17",
    ChapterNumber = 1,
    Description = "We kept on ascending, with occasional periods of quick descent, but in the main always ascending. Suddenly, I became conscious of the fact that the driver was in the act of pulling up the horses in the courtyard of a vast ruined castle, from whose tall black windows came no ray of light, and whose broken battlements showed a jagged line against the moonlit sky.\n",
    HtmlDescription = "<p>We kept on ascending, with occasional periods of quick descent, but in the main always ascending. Suddenly, I became conscious of the fact that the driver was in the act of pulling up the horses in the courtyard of a vast ruined castle, from whose tall black windows came no ray of light, and whose broken battlements showed a jagged line against the moonlit sky.</p>\n",
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
    Audiobook = new AudiobookBase
    {
        Authors = new List<AuthorObject>
        {
            new AuthorObject
            {
                Name = "name0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        AvailableMarkets = new List<string>
        {
            "available_markets2",
            "available_markets3",
            "available_markets4",
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
                Url = "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                Height = 300,
                Width = 300,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Languages = new List<string>
        {
            "languages3",
            "languages4",
        },
        MediaType = "media_type4",
        Name = "name8",
        Narrators = new List<NarratorObject>
        {
            new NarratorObject
            {
                Name = "name0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Publisher = "publisher4",
        Type = "audiobook",
        Uri = "uri2",
        TotalChapters = 186,
        Edition = "Unabridged",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    AvailableMarkets = new List<string>
    {
        "available_markets4",
    },
    ResumePoint = new ResumePointObject
    {
        FullyPlayed = false,
        ResumePositionMs = 254,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Restrictions = new ChapterRestrictionObject
    {
        Reason = "reason0",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



