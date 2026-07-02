# V2 Databases Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DatabasesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Databases` | [`List<Database1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/database-1.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2DatabasesResponse v2DatabasesResponse = new V2DatabasesResponse
{
    Databases = new List<Database1>
    {
        new Database1
        {
            Engine = Engine1.Redis,
            Name = "name6",
            NumNodes = 242,
            Region = "region2",
            Size = "size4",
            Connection = new Connection
            {
                Database = "database2",
                Host = "host0",
                Password = "password2",
                Port = 174,
                Ssl = false,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            CreatedAt = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            DbNames = new List<string>
            {
                "db_names7",
                "db_names8",
            },
            Id = new Guid("0000031c-0000-0000-0000-000000000000"),
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



