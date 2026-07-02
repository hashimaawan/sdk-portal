# V2 Databases Online Migration Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesOnlineMigrationResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*string` | Optional | The time the migration was initiated, in ISO 8601 format. |
| `Id` | `*string` | Optional | The ID of the most recent migration. |
| `Status` | [`*models.Status5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-5.md) | Optional | The current status of the migration. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DatabasesOnlineMigrationResponse := models.V2DatabasesOnlineMigrationResponse{
        CreatedAt:             models.ToPointer("2020-10-29T15:57:38Z"),
        Id:                    models.ToPointer("77b28fc8-19ff-11eb-8c9c-c68e24557488"),
        Status:                models.ToPointer(models.Status5_Running),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



