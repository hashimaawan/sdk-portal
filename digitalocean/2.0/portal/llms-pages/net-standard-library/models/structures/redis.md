# Redis

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlZGlz

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Redis`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Regions` | `List<string>` | Optional, Read-only | An array of strings containing the names of available regions |
| `Versions` | `List<string>` | Optional, Read-only | An array of strings containing the names of available regions |
| `Layouts` | [`List<Layout>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/layout.md) | Optional, Read-only | An array of objects, each indicating the node sizes (otherwise referred to as slugs) that are available with various numbers of nodes in the database cluster. Each slugs denotes the node's identifier, CPU, and RAM (in that order). |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Redis redis = new Redis
{
    Regions = new List<string>
    {
        "ams3",
        "blr1",
    },
    Versions = new List<string>
    {
        "4.4",
        "5.0",
    },
    Layouts = new List<Layout>
    {
        new Layout
        {
            NumNodes = 190,
            Sizes = new List<string>
            {
                "sizes2",
                "sizes3",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



