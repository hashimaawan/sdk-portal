# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type object.*


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Images` | [`List<Image>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Required | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
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
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
            OsFlavor = OsFlavor.Ubuntu,
            OsVersion = "20.04",
            Protection = new Protection
            {
                Delete = false,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Status = Status24.Available,
            Type = Type22.Snapshot,
            RapidDeploy = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



