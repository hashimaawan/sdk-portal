# Database

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRhdGFiYXNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Database`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ClusterName` | `*string` | Optional | The name of the underlying DigitalOcean DBaaS cluster. This is required for production databases. For dev databases, if cluster_name is not set, a new cluster will be provisioned. |
| `DbName` | `*string` | Optional | The name of the MySQL or PostgreSQL database to configure. |
| `DbUser` | `*string` | Optional | The name of the MySQL or PostgreSQL user to configure. |
| `Engine` | [`*models.Engine`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/engine.md) | Optional | - MYSQL: MySQL<br>- PG: PostgreSQL<br>- REDIS: Redis<br><br>**Default**: `"UNSET"` |
| `Name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `Production` | `*bool` | Optional | Whether this is a production or dev database. |
| `Version` | `*string` | Optional | The version of the database engine |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    database := models.Database{
        ClusterName:           models.ToPointer("cluster_name"),
        DbName:                models.ToPointer("my_db"),
        DbUser:                models.ToPointer("superuser"),
        Engine:                models.ToPointer(models.Engine_Pg),
        Name:                  "prod-db",
        Production:            models.ToPointer(true),
        Version:               models.ToPointer("12"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



