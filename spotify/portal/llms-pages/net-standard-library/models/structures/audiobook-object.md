# Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkF1ZGlvYm9va09iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`AudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Authors` | [`List<AuthorObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/author-object.md) | Required | The author(s) for the audiobook. |
| `AvailableMarkets` | `List<string>` | Required | A list of the countries in which the audiobook can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `Copyrights` | [`List<CopyrightObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/copyright-object.md) | Required | The copyright statements of the audiobook. |
| `Description` | `string` | Required | A description of the audiobook. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `HtmlDescription` | `string` | Required | A description of the audiobook. This field may contain HTML tags. |
| `Edition` | `string` | Optional | The edition of the audiobook. |
| `Explicit` | `bool` | Required | Whether or not the audiobook has explicit content (true = yes it does; false = no it does not OR unknown). |
| `ExternalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/external-url-object.md) | Required | External URLs for this audiobook. |
| `Href` | `string` | Required | A link to the Web API endpoint providing full details of the audiobook. |
| `Id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `Images` | [`List<ImageObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/image-object.md) | Required | The cover art for the audiobook in various sizes, widest first. |
| `Languages` | `List<string>` | Required | A list of the languages used in the audiobook, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `MediaType` | `string` | Required | The media type of the audiobook. |
| `Name` | `string` | Required | The name of the audiobook. |
| `Narrators` | [`List<NarratorObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/narrator-object.md) | Required | The narrator(s) for the audiobook. |
| `Publisher` | `string` | Required | The publisher of the audiobook. |
| `Type` | `string` | Required, Constant | The object type.<br><br>**Value**: `"audiobook"` |
| `Uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `TotalChapters` | `int` | Required | The number of chapters in this audiobook. |
| `Chapters` | [`PagingSimplifiedChapterObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/paging-simplified-chapter-object.md) | Required | The chapters of the audiobook. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

AudiobookObject audiobookObject = new AudiobookObject
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
        "available_markets4",
        "available_markets5",
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
    Description = "description0",
    HtmlDescription = "html_description0",
    MExplicit = false,
    ExternalUrls = new ExternalUrlObject
    {
        Spotify = "spotify6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Href = "href2",
    Id = "id0",
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
        "languages1",
        "languages2",
        "languages3",
    },
    MediaType = "media_type2",
    Name = "name0",
    Narrators = new List<NarratorObject>
    {
        new NarratorObject
        {
            Name = "name0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Publisher = "publisher2",
    Type = "audiobook",
    Uri = "uri4",
    TotalChapters = 72,
    Chapters = new PagingSimplifiedChapterObject
    {
        Href = "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
        Limit = 20,
        Next = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
        Offset = 0,
        Previous = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
        Total = 4,
        Items = new List<ChapterBase>
        {
            new ChapterBase
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
                AvailableMarkets = new List<string>
                {
                    "available_markets2",
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
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Edition = "Unabridged",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



