# V2 Databases Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9wdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DatabasesOptionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Options` | [`Options`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/options.md) | Optional | - |
| `VersionAvailability` | [`VersionAvailability`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/version-availability.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2DatabasesOptionsResponse v2DatabasesOptionsResponse = new V2DatabasesOptionsResponse
{
    Options = new Options
    {
        Mongodb = new Mongodb
        {
            Regions = new List<string>
            {
                "regions3",
                "regions4",
            },
            Versions = new List<string>
            {
                "versions3",
                "versions4",
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
        },
        Mysql = new Mysql
        {
            Regions = new List<string>
            {
                "regions9",
                "regions0",
                "regions1",
            },
            Versions = new List<string>
            {
                "versions9",
                "versions0",
                "versions1",
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
        },
        Pg = new Pg
        {
            Regions = new List<string>
            {
                "regions3",
            },
            Versions = new List<string>
            {
                "versions3",
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
        },
        Redis = new Redis
        {
            Regions = new List<string>
            {
                "regions7",
            },
            Versions = new List<string>
            {
                "versions7",
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
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    VersionAvailability = new VersionAvailability
    {
        Mongodb = new List<Mongodb1>
        {
            new Mongodb1
            {
                EndOfAvailability = "end_of_availability4",
                EndOfLife = "end_of_life4",
                Version = "version4",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Mongodb1
            {
                EndOfAvailability = "end_of_availability4",
                EndOfLife = "end_of_life4",
                Version = "version4",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Mysql = new List<Mongodb1>
        {
            new Mongodb1
            {
                EndOfAvailability = "end_of_availability0",
                EndOfLife = "end_of_life0",
                Version = "version0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Mongodb1
            {
                EndOfAvailability = "end_of_availability0",
                EndOfLife = "end_of_life0",
                Version = "version0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Pg = new List<Mongodb1>
        {
            new Mongodb1
            {
                EndOfAvailability = "end_of_availability4",
                EndOfLife = "end_of_life4",
                Version = "version4",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Redis = new List<Mongodb1>
        {
            new Mongodb1
            {
                EndOfAvailability = "end_of_availability8",
                EndOfLife = "end_of_life8",
                Version = "version8",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



