# V2 Databases Replicas Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlcGxpY2FzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesReplicasResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Replicas` | [`[]models.Replica`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/replica.md) | Optional | - |
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
    v2DatabasesReplicasResponse := models.V2DatabasesReplicasResponse{
        Replicas:              []models.Replica{
            models.Replica{
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
                CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                Id:                    models.ToPointer(uuid.MustParse("000022b6-0000-0000-0000-000000000000")),
                Name:                  "name6",
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
                PrivateNetworkUuid:    models.ToPointer("private_network_uuid6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Replica{
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
                CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                Id:                    models.ToPointer(uuid.MustParse("000022b6-0000-0000-0000-000000000000")),
                Name:                  "name6",
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
                PrivateNetworkUuid:    models.ToPointer("private_network_uuid6"),
                AdditionalProperties:  map[string]interface{}{
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



