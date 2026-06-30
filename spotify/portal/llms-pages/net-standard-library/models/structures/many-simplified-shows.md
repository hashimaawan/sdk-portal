# Many Simplified Shows

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRk1hbnlTaW1wbGlmaWVkU2hvd3M

*This model accepts additional fields of type object.*


# Class Name

`ManySimplifiedShows`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Shows` | [`List<ShowBase>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/show-base.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

ManySimplifiedShows manySimplifiedShows = new ManySimplifiedShows
{
    Shows = new List<ShowBase>
    {
        new ShowBase
        {
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
            Description = "description8",
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
            IsExternallyHosted = false,
            Languages = new List<string>
            {
                "languages5",
            },
            MediaType = "media_type4",
            Name = "name8",
            Publisher = "publisher4",
            Type = "show",
            Uri = "uri2",
            TotalEpisodes = 196,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



