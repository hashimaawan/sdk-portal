# V2 Databases Pools Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesPoolsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pools` | [`[]models.Pool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/pool.md) | Optional, Read-only | An array of connection pool objects. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DatabasesPoolsResponse := models.V2DatabasesPoolsResponse{
        Pools:                 []models.Pool{
            models.Pool{
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
                Db:                    "db2",
                Mode:                  "mode0",
                Name:                  "name2",
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
                Size:                  68,
                User:                  models.ToPointer("user2"),
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



