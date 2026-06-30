# Saved Episode Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNhdmVkRXBpc29kZU9iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`SavedEpisodeObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddedAt` | `DateTime?` | Optional | The date and time the episode was saved.<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ. |
| `Episode` | [`EpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/episode-object.md) | Optional | Information about the episode. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

SavedEpisodeObject savedEpisodeObject = new SavedEpisodeObject
{
    AddedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Episode = new EpisodeObject
    {
        AudioPreviewUrl = "audio_preview_url8",
        Description = "description2",
        HtmlDescription = "html_description8",
        DurationMs = 46,
        MExplicit = false,
        ExternalUrls = new ExternalUrlObject
        {
            Spotify = "spotify6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Href = "href4",
        Id = "id2",
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
        IsExternallyHosted = false,
        IsPlayable = false,
        Languages = new List<string>
        {
            "languages9",
            "languages0",
            "languages1",
        },
        Name = "name2",
        ReleaseDate = "release_date0",
        ReleaseDatePrecision = ReleaseDatePrecision.Year,
        Type = "type8",
        Uri = "uri6",
        Show = new ShowBase
        {
            AvailableMarkets = new List<string>
            {
                "available_markets0",
                "available_markets1",
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
            Description = "description4",
            HtmlDescription = "html_description4",
            MExplicit = false,
            ExternalUrls = new ExternalUrlObject
            {
                Spotify = "spotify6",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Href = "href8",
            Id = "id6",
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
            IsExternallyHosted = false,
            Languages = new List<string>
            {
                "languages7",
                "languages6",
                "languages5",
            },
            MediaType = "media_type6",
            Name = "name6",
            Publisher = "publisher6",
            Type = "type4",
            Uri = "uri0",
            TotalEpisodes = 198,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Language = "language4",
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
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



