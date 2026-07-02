# V2 Databases Online Migration Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesOnlineMigrationRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DisableSsl` | `*bool` | Optional | Enables SSL encryption when connecting to the source database. |
| `Source` | [`*models.Source`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/source.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DatabasesOnlineMigrationRequest := models.V2DatabasesOnlineMigrationRequest{
        DisableSsl:            models.ToPointer(false),
        Source:                models.ToPointer(models.Source{
            Database:              models.ToPointer("database4"),
            Host:                  models.ToPointer("host4"),
            Password:              models.ToPointer("password8"),
            Port:                  models.ToPointer(180),
            Ssl:                   models.ToPointer(false),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



