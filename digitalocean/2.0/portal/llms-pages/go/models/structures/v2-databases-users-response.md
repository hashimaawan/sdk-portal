# V2 Databases Users Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVzZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesUsersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Users` | [`[]models.User`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/user.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DatabasesUsersResponse := models.V2DatabasesUsersResponse{
        Users:                 []models.User{
            models.User{
                MysqlSettings:         models.ToPointer(models.MysqlSettings{
                    AuthPlugin:            models.AuthPlugin_MysqlNativePassword,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Name:                  "name6",
                Password:              models.ToPointer("password0"),
                Role:                  models.ToPointer(models.Role_Primary),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.User{
                MysqlSettings:         models.ToPointer(models.MysqlSettings{
                    AuthPlugin:            models.AuthPlugin_MysqlNativePassword,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Name:                  "name6",
                Password:              models.ToPointer("password0"),
                Role:                  models.ToPointer(models.Role_Primary),
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



