# Paged Categories

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2VkQ2F0ZWdvcmllcw

*This model accepts additional fields of type object.*


# Class Name

`PagedCategories`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Categories` | [`Categories`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/categories.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

PagedCategories pagedCategories = new PagedCategories
{
    Categories = new Categories
    {
        Href = "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
        Limit = 20,
        Next = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
        Offset = 0,
        Previous = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
        Total = 4,
        Items = new List<CategoryObject>
        {
            new CategoryObject
            {
                Href = "href0",
                Icons = new List<ImageObject>
                {
                    new ImageObject
                    {
                        Url = "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                        Height = 300,
                        Width = 300,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Id = "equal",
                Name = "EQUAL",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



