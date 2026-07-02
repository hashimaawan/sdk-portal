# V2 Projects Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2ProjectsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Projects` | [`List<Project>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/project.md) | Optional | - |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/links.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2ProjectsResponse v2ProjectsResponse = new V2ProjectsResponse
{
    Meta = new Meta
    {
        Total = 2,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Projects = new List<Project>
    {
        new Project
        {
            CreatedAt = DateTime.ParseExact("2018-09-27T20:10:35Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Description = "My website API",
            Environment = Environment.Production,
            Id = new Guid("4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679"),
            Name = "my-web-api",
            OwnerId = 258992,
            OwnerUuid = "99525febec065ca37b2ffe4f852fd2b2581895e7",
            Purpose = "Service or API",
            UpdatedAt = DateTime.ParseExact("2018-09-27T20:10:35Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            IsDefault = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Project
        {
            CreatedAt = DateTime.ParseExact("2017-10-19T21:44:20Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Description = "Default project",
            Environment = Environment.Development,
            Id = new Guid("addb4547-6bab-419a-8542-76263a033cf6"),
            Name = "Default",
            OwnerId = 258992,
            OwnerUuid = "99525febec065ca37b2ffe4f852fd2b2581895e7",
            Purpose = "Just trying out DigitalOcean",
            UpdatedAt = DateTime.ParseExact("2019-11-05T18:50:03Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            IsDefault = true,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Links = new Links
    {
        Pages = LinksPages.FromPages(
            new Pages
            {
                Last = "https://api.digitalocean.com/v2/projects?page=1",
                Next = "next2",
                ["first"] = ApiHelper.JsonDeserialize<object>("\"https://api.digitalocean.com/v2/projects?page=1\""),
            }
        ),
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



