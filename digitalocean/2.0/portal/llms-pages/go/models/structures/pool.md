# Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlBvb2w

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Pool`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Connection` | [`*models.Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/connection.md) | Optional | - |
| `Db` | `string` | Required | The database for use with the connection pool. |
| `Mode` | `string` | Required | The PGBouncer transaction mode for the connection pool. The allowed values are session, transaction, and statement. |
| `Name` | `string` | Required | A unique name for the connection pool. Must be between 3 and 60 characters. |
| `PrivateConnection` | [`*models.PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/private-connection.md) | Optional | - |
| `Size` | `int` | Required | The desired size of the PGBouncer connection pool. The maximum allowed size is determined by the size of the cluster's primary node. 25 backend server connections are allowed for every 1GB of RAM. Three are reserved for maintenance. For example, a primary node with 1 GB of RAM allows for a maximum of 22 backend server connections while one with 4 GB would allow for 97. Note that these are shared across all connection pools in a cluster. |
| `User` | `*string` | Optional | The name of the user for use with the connection pool. When excluded, all sessions connect to the database as the inbound user. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    pool := models.Pool{
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
    }

}
```



