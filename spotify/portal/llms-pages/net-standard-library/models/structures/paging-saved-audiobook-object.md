# Paging Saved Audiobook Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2luZ1NhdmVkQXVkaW9ib29rT2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`PagingSavedAudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `Limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `string` | Required | URL to the next page of items. ( `null` if none) |
| `Offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `Previous` | `string` | Required | URL to the previous page of items. ( `null` if none) |
| `Total` | `int` | Required | The total number of items available to return. |
| `Items` | [`List<SavedAudiobookObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/saved-audiobook-object.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

PagingSavedAudiobookObject pagingSavedAudiobookObject = new PagingSavedAudiobookObject
{
    Href = "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
    Limit = 20,
    Next = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
    Offset = 0,
    Previous = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
    Total = 4,
    Items = new List<SavedAudiobookObject>
    {
        new SavedAudiobookObject
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
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



