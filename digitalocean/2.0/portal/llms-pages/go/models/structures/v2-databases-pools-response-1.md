# V2 Databases Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesPoolsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pool` | [`models.Pool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/pool.md) | Required | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DatabasesPoolsResponse1 := models.V2DatabasesPoolsResponse1{
        Pool:                  models.Pool{
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
            Db:                    "defaultdb",
            Mode:                  "transaction",
            Name:                  "backend-pool",
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
            Size:                  10,
            User:                  models.ToPointer("doadmin"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



