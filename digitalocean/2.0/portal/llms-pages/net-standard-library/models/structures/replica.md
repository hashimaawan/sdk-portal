# Replica

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlcGxpY2E

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Replica`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Connection` | [`Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/connection.md) | Optional | - |
| `CreatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. |
| `Id` | `Guid?` | Optional, Read-only | A unique ID that can be used to identify and reference a database replica. |
| `Name` | `string` | Required | The name to give the read-only replicating |
| `PrivateConnection` | [`PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/private-connection.md) | Optional | - |
| `PrivateNetworkUuid` | `string` | Optional | A string specifying the UUID of the VPC to which the read-only replica will be assigned. If excluded, the replica will be assigned to your account's default VPC for the region. |
| `Region` | `string` | Optional | A slug identifier for the region where the read-only replica will be located. If excluded, the replica will be placed in the same region as the cluster. |
| `Size` | `string` | Optional | A slug identifier representing the size of the node for the read-only replica. The size of the replica must be at least as large as the node size for the database cluster from which it is replicating. |
| `Status` | [`Status4?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. |
| `Tags` | `List<string>` | Optional | A flat array of tag names as strings to apply to the read-only replica after it is created. Tag names can either be existing or new tags. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Replica replica = new Replica
{
    Name = "read-nyc3-01",
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
    Id = new Guid("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30"),
    PrivateConnection = new PrivateConnection
    {
        Database = "database4",
        Host = "host4",
        Password = "password8",
        Port = 228,
        Ssl = false,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    PrivateNetworkUuid = "9423cbad-9211-442f-820b-ef6915e99b5f",
    Region = "nyc3",
    Size = "db-s-2vcpu-4gb",
    Status = Status4.Creating,
    Tags = new List<string>
    {
        "production",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



