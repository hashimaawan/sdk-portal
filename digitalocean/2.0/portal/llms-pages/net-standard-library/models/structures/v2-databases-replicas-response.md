# V2 Databases Replicas Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlcGxpY2FzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DatabasesReplicasResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Replicas` | [`List<Replica>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/replica.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2DatabasesReplicasResponse v2DatabasesReplicasResponse = new V2DatabasesReplicasResponse
{
    Replicas = new List<Replica>
    {
        new Replica
        {
            Name = "name6",
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
            Id = new Guid("000022b6-0000-0000-0000-000000000000"),
            PrivateConnection = new PrivateConnection
            {
                Database = "database4",
                Host = "host4",
                Password = "password8",
                Port = 228,
                Ssl = false,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            PrivateNetworkUuid = "private_network_uuid6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Replica
        {
            Name = "name6",
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
            Id = new Guid("000022b6-0000-0000-0000-000000000000"),
            PrivateConnection = new PrivateConnection
            {
                Database = "database4",
                Host = "host4",
                Password = "password8",
                Port = 228,
                Ssl = false,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            PrivateNetworkUuid = "private_network_uuid6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



