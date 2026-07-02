# V2 Projects Default Resources Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2ProjectsDefaultResourcesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Resources` | [`List<Resources1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/resources-1.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2ProjectsDefaultResourcesResponse1 v2ProjectsDefaultResourcesResponse1 = new V2ProjectsDefaultResourcesResponse1
{
    Resources = new List<Resources1>
    {
        new Resources1
        {
            AssignedAt = DateTime.ParseExact("2018-09-28T19:26:37Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Links = new Links4
            {
                Self = "https://api.digitalocean.com/v2/droplets/13457723",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Status = Status14.Ok,
            Urn = "do:droplet:13457723",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Resources1
        {
            AssignedAt = DateTime.ParseExact("2019-03-31T16:24:14Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Links = new Links4
            {
                Self = "https://api.digitalocean.com/v2/domains/example.com",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Status = Status14.Ok,
            Urn = "do:domain:example.com",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



