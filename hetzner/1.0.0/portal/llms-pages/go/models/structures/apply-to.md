# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFwcGx5VG8

*This model accepts additional fields of type interface{}.*


# Class Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LabelSelector` | [`*models.LabelSelector1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` |
| `Server` | [`*models.Server2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` |
| `Type` | [`models.Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-7.md) | Required | Type of the resource |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    applyTo := models.ApplyTo{
        LabelSelector:         models.ToPointer(models.LabelSelector1{
            Selector:              "selector8",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Server:                models.ToPointer(models.Server2{
            Id:                    14,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Type:                  models.Type7_Server,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



