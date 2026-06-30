# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Images` | [`List<Image>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/image.md) | Required | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ImagesResponse imagesResponse = new ImagesResponse
{
    Images = new List<Image>
    {
        new Image
        {
            BoundTo = null,
            Created = "2016-01-30T23:55:00+00:00",
            CreatedFrom = new CreatedFrom
            {
                Id = 1,
                Name = "Server",
            },
            Deleted = null,
            Deprecated = "2018-02-28T00:00:00+00:00",
            Description = "Ubuntu 20.04 Standard 64 bit",
            DiskSize = 10,
            Id = 42,
            ImageSize = 2.3,
            Labels = new Dictionary<string, string>
            {
                ["key0"] = "labels0",
                ["key1"] = "labels1",
            },
            Name = "ubuntu-20.04",
            OsFlavor = OsFlavorEnum.Ubuntu,
            OsVersion = "20.04",
            Protection = new Protection
            {
                Delete = false,
            },
            Status = Status24Enum.Available,
            Type = Type22Enum.Snapshot,
            RapidDeploy = false,
        },
    },
    Meta = new Meta
    {
        Pagination = new Pagination
        {
            LastPage = 77.7,
            NextPage = 209.18,
            Page = 17.58,
            PerPage = 13.34,
            PreviousPage = 50.02,
            TotalEntries = 206.64,
        },
    },
};
```



