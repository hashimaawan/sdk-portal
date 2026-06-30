# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlJlc291cmNl

*This model accepts additional fields of type interface{}.*


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Item` | [`*models.Item2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/item-2.md) | Optional | - |
| `ItemVersion` | `*int` | Optional | - |
| `Type` | [`*models.Type`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/enumerations/type.md) | Optional | - |
| `Vault` | [`*models.Vault3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/vault-3.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    resource := models.Resource{
        Item:                  models.ToPointer(models.Item2{
            Id:                    models.ToPointer("id2"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        ItemVersion:           models.ToPointer(108),
        Type:                  models.ToPointer(models.Type_Item),
        Vault:                 models.ToPointer(models.Vault3{
            Id:                    models.ToPointer("id6"),
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



