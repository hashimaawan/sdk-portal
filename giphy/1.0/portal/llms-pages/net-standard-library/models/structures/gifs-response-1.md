# Gifs Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdpZnMlMjUyMFJlc3BvbnNlMQ


# Class Name

`GifsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Data` | [`Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/gif.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |


# Example

```csharp
using GiphyAPI.Standard.Models;
using System.Collections.Generic;
using System.Globalization;

GifsResponse1 gifsResponse1 = new GifsResponse1
{
    Data = new Gif
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
    },
    Meta = new Meta
    {
        Msg = "msg8",
        ResponseId = "response_id0",
        Status = 98,
    },
};
```



