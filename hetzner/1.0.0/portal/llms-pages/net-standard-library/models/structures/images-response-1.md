# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type object.*


# Class Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

ImagesResponse1 imagesResponse1 = new ImagesResponse1
{
    Image = new Image
    {
        BoundTo = 186,
        Created = "created6",
        CreatedFrom = new CreatedFrom
        {
            Id = 60,
            Name = "name6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Deleted = "deleted4",
        Deprecated = "deprecated8",
        Description = "description6",
        DiskSize = 244.18,
        Id = 128,
        ImageSize = 141.34,
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels4",
        },
        Name = "name6",
        OsFlavor = OsFlavor.Debian,
        OsVersion = "os_version4",
        Protection = new Protection
        {
            Delete = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Status = Status24.Unavailable,
        Type = Type22.App,
        RapidDeploy = false,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



