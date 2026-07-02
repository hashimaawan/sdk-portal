# V2 Images Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2ImagesResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Image` | [`Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/image-1.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2ImagesResponse2 v2ImagesResponse2 = new V2ImagesResponse2
{
    Image = new Image1
    {
        CreatedAt = DateTime.ParseExact("2020-05-04T22:23:02Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        Description = "description6",
        Distribution = Distribution.Ubuntu,
        ErrorMessage = "error_message8",
        Id = 7555620,
        MinDiskSize = 20,
        Name = "Nifty New Snapshot",
        MPublic = true,
        Regions = new List<Region2>
        {
            Region2.Nyc1,
            Region2.Nyc2,
        },
        SizeGigabytes = 2.34,
        Slug = "nifty1",
        Status = Status7.New,
        Tags = new List<string>
        {
            "base-image",
            "prod",
        },
        Type = Type9.Snapshot,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



