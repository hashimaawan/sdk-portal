# V2 Volumes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2VolumesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Volumes` | [`List<Volume>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/volume.md) | Required | Array of volumes. |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/links.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2VolumesResponse v2VolumesResponse = new V2VolumesResponse
{
    Volumes = new List<Volume>
    {
        new Volume
        {
            CreatedAt = "2020-03-02T17:00:49Z",
            Description = "Block store for examples",
            DropletIds = new List<int>
            {

            },
            Id = "506f78a4-e098-11e5-ad9f-000f53306ae1",
            Name = "example",
            SizeGigabytes = 10,
            Tags = new List<string>
            {
                "base-image",
                "prod",
            },
            FilesystemLabel = "example",
            FilesystemType = "ext4",
            Region = new Region
            {
                Available = true,
                Features = new List<string>
                {
                    "private_networking",
                    "backups",
                    "ipv6",
                    "metadata",
                },
                Name = "New York 1",
                Sizes = new List<string>
                {
                    "s-1vcpu-1gb",
                    "s-1vcpu-2gb",
                    "s-1vcpu-3gb",
                    "s-2vcpu-2gb",
                    "s-3vcpu-1gb",
                    "s-2vcpu-4gb",
                    "s-4vcpu-8gb",
                    "s-6vcpu-16gb",
                    "s-8vcpu-32gb",
                    "s-12vcpu-48gb",
                    "s-16vcpu-64gb",
                    "s-20vcpu-96gb",
                    "s-24vcpu-128gb",
                    "s-32vcpu-192gb",
                },
                Slug = "nyc1",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Meta = new Meta
    {
        Total = 1,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Links = new Links
    {
        Pages = LinksPages.FromPages(
            new Pages
            {
                Last = "last6",
                Next = "next2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



