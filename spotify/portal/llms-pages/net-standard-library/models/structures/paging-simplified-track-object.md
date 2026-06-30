# Paging Simplified Track Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2luZ1NpbXBsaWZpZWRUcmFja09iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`PagingSimplifiedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `Limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `string` | Required | URL to the next page of items. ( `null` if none) |
| `Offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `Previous` | `string` | Required | URL to the previous page of items. ( `null` if none) |
| `Total` | `int` | Required | The total number of items available to return. |
| `Items` | [`List<SimplifiedTrackObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/simplified-track-object.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

PagingSimplifiedTrackObject pagingSimplifiedTrackObject = new PagingSimplifiedTrackObject
{
    Href = "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
    Limit = 20,
    Next = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
    Offset = 0,
    Previous = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
    Total = 4,
    Items = new List<SimplifiedTrackObject>
    {
        new SimplifiedTrackObject
        {
            Artists = new List<SimplifiedArtistObject>
            {
                new SimplifiedArtistObject
                {
                    ExternalUrls = new ExternalUrlObject
                    {
                        Spotify = "spotify6",
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                    Href = "href2",
                    Id = "id0",
                    Name = "name0",
                    Type = SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models.Type.Artist,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            AvailableMarkets = new List<string>
            {
                "available_markets2",
            },
            DiscNumber = 244,
            DurationMs = 52,
            MExplicit = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



