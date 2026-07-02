# V2 Databases Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Connection` | [`*models.Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/connection.md) | Optional | - |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. |
| `DbNames` | `models.Optional[[]string]` | Optional, Read-only | An array of strings containing the names of databases created in the database cluster. |
| `Engine` | [`models.Engine1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/engine-1.md) | Required | A slug representing the database engine used for the cluster. The possible values are: "pg" for PostgreSQL, "mysql" for MySQL, "redis" for Redis, and "mongodb" for MongoDB. |
| `Id` | `*uuid.UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a database cluster. |
| `MaintenanceWindow` | [`models.Optional[models.MaintenanceWindow]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/maintenance-window.md) | Optional | - |
| `Name` | `string` | Required | A unique, human-readable name referring to a database cluster. |
| `NumNodes` | `int` | Required | The number of nodes in the database cluster. |
| `PrivateConnection` | [`*models.PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/private-connection.md) | Optional | - |
| `PrivateNetworkUuid` | `*string` | Optional | A string specifying the UUID of the VPC to which the database cluster will be assigned. If excluded, the cluster when creating a new database cluster, it will be assigned to your account's default VPC for the region.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` |
| `ProjectId` | `*uuid.UUID` | Optional | The ID of the project that the database cluster is assigned to. If excluded when creating a new database cluster, it will be assigned to your default project. |
| `Region` | `string` | Required | The slug identifier for the region where the database cluster is located. |
| `Rules` | [`[]models.Rule1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/rule-1.md) | Optional | - |
| `Size` | `string` | Required | The slug identifier representing the size of the nodes in the database cluster. |
| `Status` | [`*models.Status4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. |
| `Tags` | `models.Optional[[]string]` | Optional | An array of tags that have been applied to the database cluster. |
| `Users` | [`models.Optional[[]models.User]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/user.md) | Optional, Read-only | - |
| `Version` | `*string` | Optional | A string representing the version of the database engine in use for the cluster. |
| `VersionEndOfAvailability` | `*string` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. |
| `VersionEndOfLife` | `*string` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. |
| `BackupRestore` | [`*models.BackupRestore`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/backup-restore.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    v2DatabasesRequest := models.V2DatabasesRequest{
        Connection:               models.ToPointer(models.Connection{
            Database:              models.ToPointer("database2"),
            Host:                  models.ToPointer("host0"),
            Password:              models.ToPointer("password2"),
            Port:                  models.ToPointer(174),
            Ssl:                   models.ToPointer(false),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        CreatedAt:                models.ToPointer(parseTime(time.RFC3339, "2019-01-11T18:37:36Z", func(err error) { log.Fatalln(err) })),
        DbNames:                  models.NewOptional(models.ToPointer([]string{
            "doadmin",
        })),
        Engine:                   models.Engine1_Pg,
        Id:                       models.ToPointer(uuid.MustParse("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30")),
        MaintenanceWindow:        models.NewOptional(models.ToPointer(models.MaintenanceWindow{
            Day:                   "day0",
            Description:           []string{
                "description3",
                "description2",
            },
            Hour:                  "hour8",
            Pending:               models.ToPointer(false),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        })),
        Name:                     "backend",
        NumNodes:                 2,
        PrivateNetworkUuid:       models.ToPointer("d455e75d-4858-4eec-8c95-da2f0a5f93a7"),
        ProjectId:                models.ToPointer(uuid.MustParse("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30")),
        Region:                   "nyc3",
        Size:                     "db-s-2vcpu-4gb",
        Status:                   models.ToPointer(models.Status4_Creating),
        Tags:                     models.NewOptional(models.ToPointer([]string{
            "production",
        })),
        Version:                  models.ToPointer("10"),
        VersionEndOfAvailability: models.ToPointer("2023-05-09T00:00:00Z"),
        VersionEndOfLife:         models.ToPointer("2023-11-09T00:00:00Z"),
        AdditionalProperties:     map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



