# Options

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk9wdGlvbnM

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Options`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Mongodb` | [`Mongodb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/mongodb.md) | Optional | - |
| `Mysql` | [`Mysql`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/mysql.md) | Optional | - |
| `Pg` | [`Pg`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/pg.md) | Optional | - |
| `Redis` | [`Redis`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/redis.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Options options = new Options
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
};
```



