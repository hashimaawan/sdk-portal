# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlVzZXI

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`User`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `MysqlSettings` | [`*models.MysqlSettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/mysql-settings.md) | Optional | - |
| `Name` | `string` | Required | The name of a database user. |
| `Password` | `*string` | Optional, Read-only | A randomly generated password for the database user. |
| `Role` | [`*models.Role`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/role.md) | Optional, Read-only | A string representing the database user's role. The value will be either<br>"primary" or "normal". |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    user := models.User{
        MysqlSettings:         models.ToPointer(models.MysqlSettings{
            AuthPlugin:            models.AuthPlugin_MysqlNativePassword,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Name:                  "app-01",
        Password:              models.ToPointer("jge5lfxtzhx42iff"),
        Role:                  models.ToPointer(models.Role_Normal),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



