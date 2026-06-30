# Paging Simplified Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2luZ1NpbXBsaWZpZWRBdWRpb2Jvb2tPYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`PagingSimplifiedAudiobookObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `Limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `string` | Required | URL to the next page of items. ( `null` if none) |
| `Offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `Previous` | `string` | Required | URL to the previous page of items. ( `null` if none) |
| `Total` | `int` | Required | The total number of items available to return. |
| `Items` | [`List<AudiobookBase>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/audiobook-base.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

PagingSimplifiedAudiobookObject pagingSimplifiedAudiobookObject = new PagingSimplifiedAudiobookObject
{
    Href = "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
    Limit = 20,
    Next = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
    Offset = 0,
    Previous = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
    Total = 4,
    Items = new List<AudiobookBase>
    {
        new AudiobookBase
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
                "languages5",
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
            TotalChapters = 202,
            Edition = "Unabridged",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



