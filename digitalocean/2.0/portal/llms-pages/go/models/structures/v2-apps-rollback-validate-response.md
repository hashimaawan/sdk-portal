# V2 Apps Rollback Validate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSb2xsYmFjayUyNTIwVmFsaWRhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2AppsRollbackValidateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`*models.Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/error.md) | Optional | - |
| `Valid` | `*bool` | Optional | Indicates whether the app can be rolled back to the specified deployment. |
| `Warnings` | [`[]models.Warning`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/warning.md) | Optional | Contains a list of warnings that may cause the rollback to run under unideal circumstances. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2AppsRollbackValidateResponse := models.V2AppsRollbackValidateResponse{
        Error:                 models.ToPointer(models.Error{
            Code:                  models.ToPointer(models.Code_IncompatiblePhase),
            Components:            []string{
                "components3",
            },
            Message:               models.ToPointer("message4"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Valid:                 models.ToPointer(false),
        Warnings:              []models.Warning{
            models.Warning{
                Code:                  models.ToPointer(models.Code_ExceededRevisionLimit),
                Components:            []string{
                    "components3",
                },
                Message:               models.ToPointer("message4"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Warning{
                Code:                  models.ToPointer(models.Code_ExceededRevisionLimit),
                Components:            []string{
                    "components3",
                },
                Message:               models.ToPointer("message4"),
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



