# Stickers Translate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/net-standard-library/x-redirect/JTI0bSUyRlN0aWNrZXJzJTI1MjBUcmFuc2xhdGUlMjUyMFJlc3BvbnNl


# Class Name

`StickersTranslateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Data` | [`Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/net-standard-library/models/structures/gif.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/net-standard-library/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |


# Example

```csharp
using GiphyAPI.Standard.Models;
using System.Collections.Generic;
using System.Globalization;

StickersTranslateResponse stickersTranslateResponse = new StickersTranslateResponse
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



