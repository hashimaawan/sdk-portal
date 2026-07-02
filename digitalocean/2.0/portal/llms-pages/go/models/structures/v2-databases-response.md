# V2 Databases Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Databases` | [`[]models.Database1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/database-1.md) | Optional | - |
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
    v2DatabasesResponse := models.V2DatabasesResponse{
        Databases:             []models.Database1{
            models.Database1{
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
                CreatedAt:                models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                DbNames:                  models.NewOptional(models.ToPointer([]string{
                    "db_names7",
                    "db_names8",
                })),
                Engine:                   models.Engine1_Redis,
                Id:                       models.ToPointer(uuid.MustParse("0000031c-0000-0000-0000-000000000000")),
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
                Name:                     "name6",
                NumNodes:                 242,
                Region:                   "region2",
                Size:                     "size4",
                AdditionalProperties:     map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



