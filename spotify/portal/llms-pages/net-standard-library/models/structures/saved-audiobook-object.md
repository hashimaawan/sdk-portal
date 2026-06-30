# Saved Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNhdmVkQXVkaW9ib29rT2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`SavedAudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddedAt` | `DateTime?` | Optional | The date and time the audiobook was saved<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. |
| `Audiobook` | [`AudiobookObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/audiobook-object.md) | Optional | Information about the audiobook. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

SavedAudiobookObject savedAudiobookObject = new SavedAudiobookObject
{
    AddedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Audiobook = new AudiobookObject
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
            new CopyrightObject
            {
                Text = "text2",
                Type = "type2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
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
            new ImageObject
            {
                Url = "url6",
                Height = 182,
                Width = 222,
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
            new NarratorObject
            {
                Name = "name0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Publisher = "publisher4",
        Type = "type2",
        Uri = "uri2",
        TotalChapters = 186,
        Chapters = new PagingSimplifiedChapterObject
        {
            Href = "href4",
            Limit = 230,
            Next = "next0",
            Offset = 122,
            Previous = "previous0",
            Total = 136,
            Items = new List<ChapterBase>
            {
                new ChapterBase
                {
                    AudioPreviewUrl = "audio_preview_url4",
                    ChapterNumber = 164,
                    Description = "description2",
                    HtmlDescription = "html_description2",
                    DurationMs = 52,
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
                    IsPlayable = false,
                    Languages = new List<string>
                    {
                        "languages5",
                    },
                    Name = "name8",
                    ReleaseDate = "release_date6",
                    ReleaseDatePrecision = ReleaseDatePrecision.Month,
                    Type = "type2",
                    Uri = "uri2",
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
        Edition = "edition8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



