# Version Availability

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlZlcnNpb25BdmFpbGFiaWxpdHk

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`VersionAvailability`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Mongodb` | [`List<Mongodb1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `Mysql` | [`List<Mongodb1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `Pg` | [`List<Mongodb1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `Redis` | [`List<Mongodb1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/mongodb-1.md) | Optional | An array of objects, each indicating the version end-of-life, end-of-availability for various database engines |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

VersionAvailability versionAvailability = new VersionAvailability
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
    Redis = new List<Mongodb1>
    {
        new Mongodb1
        {
            EndOfAvailability = "end_of_availability8",
            EndOfLife = "end_of_life8",
            Version = "version8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Mongodb1
        {
            EndOfAvailability = "end_of_availability8",
            EndOfLife = "end_of_life8",
            Version = "version8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



