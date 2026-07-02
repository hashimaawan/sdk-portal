# Mysql Settings

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk15c3FsU2V0dGluZ3M

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`MysqlSettings`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AuthPlugin` | [`models.AuthPlugin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/auth-plugin.md) | Required | A string specifying the authentication method to be used for connections<br>to the MySQL user account. The valid values are `mysql_native_password`<br>or `caching_sha2_password`. If excluded when creating a new user, the<br>default for the version of MySQL in use will be used. As of MySQL 8.0, the<br>default is `caching_sha2_password`. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    mysqlSettings := models.MysqlSettings{
        AuthPlugin:            models.AuthPlugin_MysqlNativePassword,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



