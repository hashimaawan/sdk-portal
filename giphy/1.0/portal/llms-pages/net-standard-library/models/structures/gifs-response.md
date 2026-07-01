# Gifs Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdpZnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type object.*


# Class Name

`GifsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Data` | [`List<Gif>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/gif.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |
| `Pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/pagination.md) | Optional | The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using GiphyApi.Standard.Models;
using GiphyApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

GifsResponse gifsResponse = new GifsResponse
{
    Data = new List<Gif>
    {
        new Gif
        {
            BitlyUrl = "bitly_url0",
            ContentUrl = "content_url4",
            CreateDatetime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            EmbdedUrl = "embded_url8",
            FeaturedTags = new List<string>
            {
                "featured_tags0",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Meta = new Meta
    {
        Msg = "msg8",
        ResponseId = "response_id0",
        Status = 98,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Pagination = new Pagination
    {
        Count = 192,
        Offset = 240,
        TotalCount = 100,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



