# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
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
        OsFlavor = OsFlavorEnum.Debian,
        OsVersion = "os_version4",
        Protection = new Protection
        {
            Delete = false,
        },
        Status = Status24Enum.Unavailable,
        Type = Type22Enum.App,
        RapidDeploy = false,
    },
};
```



