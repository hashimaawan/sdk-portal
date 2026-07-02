# V2 Databases Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DatabasesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | [`Database1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/database-1.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2DatabasesResponse1 v2DatabasesResponse1 = new V2DatabasesResponse1
{
    Database = new Database1
    {
        Engine = Engine1.Pg,
        Name = "backend",
        NumNodes = 2,
        Region = "nyc3",
        Size = "db-s-2vcpu-4gb",
        Connection = new Connection
        {
            Database = "database2",
            Host = "host0",
            Password = "password2",
            Port = 174,
            Ssl = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        CreatedAt = DateTime.ParseExact("2019-01-11T18:37:36Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        DbNames = new List<string>
        {
            "doadmin",
        },
        Id = new Guid("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30"),
        MaintenanceWindow = new MaintenanceWindow
        {
            Day = "day0",
            Hour = "hour8",
            Description = new List<string>
            {
                "description3",
                "description2",
            },
            Pending = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        PrivateNetworkUuid = "d455e75d-4858-4eec-8c95-da2f0a5f93a7",
        ProjectId = new Guid("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30"),
        Status = Status4.Creating,
        Tags = new List<string>
        {
            "production",
        },
        Version = "10",
        VersionEndOfAvailability = "2023-05-09T00:00:00Z",
        VersionEndOfLife = "2023-11-09T00:00:00Z",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



