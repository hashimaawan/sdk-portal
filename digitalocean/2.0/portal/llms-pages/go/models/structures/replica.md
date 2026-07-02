# Replica

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlcGxpY2E

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Replica`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Connection` | [`*models.Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/connection.md) | Optional | - |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. |
| `Id` | `*uuid.UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a database replica. |
| `Name` | `string` | Required | The name to give the read-only replicating |
| `PrivateConnection` | [`*models.PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/private-connection.md) | Optional | - |
| `PrivateNetworkUuid` | `*string` | Optional | A string specifying the UUID of the VPC to which the read-only replica will be assigned. If excluded, the replica will be assigned to your account's default VPC for the region. |
| `Region` | `*string` | Optional | A slug identifier for the region where the read-only replica will be located. If excluded, the replica will be placed in the same region as the cluster. |
| `Size` | `*string` | Optional | A slug identifier representing the size of the node for the read-only replica. The size of the replica must be at least as large as the node size for the database cluster from which it is replicating. |
| `Status` | [`*models.Status4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. |
| `Tags` | `[]string` | Optional | A flat array of tag names as strings to apply to the read-only replica after it is created. Tag names can either be existing or new tags. |
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
    replica := models.Replica{
        Connection:            models.ToPointer(models.Connection{
            Database:              models.ToPointer("database2"),
            Host:                  models.ToPointer("host0"),
            Password:              models.ToPointer("password2"),
            Port:                  models.ToPointer(174),
            Ssl:                   models.ToPointer(false),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2019-01-11T18:37:36Z", func(err error) { log.Fatalln(err) })),
        Id:                    models.ToPointer(uuid.MustParse("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30")),
        Name:                  "read-nyc3-01",
        PrivateConnection:     models.ToPointer(models.PrivateConnection{
            Database:              models.ToPointer("database4"),
            Host:                  models.ToPointer("host4"),
            Password:              models.ToPointer("password8"),
            Port:                  models.ToPointer(228),
            Ssl:                   models.ToPointer(false),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        PrivateNetworkUuid:    models.ToPointer("9423cbad-9211-442f-820b-ef6915e99b5f"),
        Region:                models.ToPointer("nyc3"),
        Size:                  models.ToPointer("db-s-2vcpu-4gb"),
        Status:                models.ToPointer(models.Status4_Creating),
        Tags:                  []string{
            "production",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



