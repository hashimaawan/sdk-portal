# Database 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGFiYXNlMQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Database1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Connection` | [`Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/connection.md) | Optional | - |
| `CreatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. |
| `DbNames` | `List<string>` | Optional, Read-only | An array of strings containing the names of databases created in the database cluster. |
| `Engine` | [`Engine1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/engine-1.md) | Required | A slug representing the database engine used for the cluster. The possible values are: "pg" for PostgreSQL, "mysql" for MySQL, "redis" for Redis, and "mongodb" for MongoDB. |
| `Id` | `Guid?` | Optional, Read-only | A unique ID that can be used to identify and reference a database cluster. |
| `MaintenanceWindow` | [`MaintenanceWindow`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/maintenance-window.md) | Optional | - |
| `Name` | `string` | Required | A unique, human-readable name referring to a database cluster. |
| `NumNodes` | `int` | Required | The number of nodes in the database cluster. |
| `PrivateConnection` | [`PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/private-connection.md) | Optional | - |
| `PrivateNetworkUuid` | `string` | Optional | A string specifying the UUID of the VPC to which the database cluster will be assigned. If excluded, the cluster when creating a new database cluster, it will be assigned to your account's default VPC for the region.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` |
| `ProjectId` | `Guid?` | Optional | The ID of the project that the database cluster is assigned to. If excluded when creating a new database cluster, it will be assigned to your default project. |
| `Region` | `string` | Required | The slug identifier for the region where the database cluster is located. |
| `Rules` | [`List<Rule1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/rule-1.md) | Optional | - |
| `Size` | `string` | Required | The slug identifier representing the size of the nodes in the database cluster. |
| `Status` | [`Status4?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. |
| `Tags` | `List<string>` | Optional | An array of tags that have been applied to the database cluster. |
| `Users` | [`List<User>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/user.md) | Optional, Read-only | - |
| `Version` | `string` | Optional | A string representing the version of the database engine in use for the cluster. |
| `VersionEndOfAvailability` | `string` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. |
| `VersionEndOfLife` | `string` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Database1 database1 = new Database1
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
};
```



