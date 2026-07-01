# Firewall Remove from Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVtb3ZlRnJvbVJlc291cmNlcw

*This model accepts additional fields of type interface{}.*


# Class Name

`FirewallRemoveFromResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LabelSelector` | [`*models.LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `Server` | [`*models.Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `Type` | [`*models.Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-7.md) | Optional | Type of the resource |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    firewallRemoveFromResources := models.FirewallRemoveFromResources{
        LabelSelector:         models.ToPointer(models.LabelSelector5{
            Selector:              "selector8",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Server:                models.ToPointer(models.Server9{
            Id:                    14,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Type:                  models.ToPointer(models.Type7_Server),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



