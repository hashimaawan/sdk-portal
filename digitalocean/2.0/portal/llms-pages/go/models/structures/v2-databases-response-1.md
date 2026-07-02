# V2 Databases Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | [`models.Database1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/database-1.md) | Required | - |
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
    v2DatabasesResponse1 := models.V2DatabasesResponse1{
        Database:              models.Database1{
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
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



