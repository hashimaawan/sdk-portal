# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type interface{}.*


# Class Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `RemoveFrom` | [`[]models.FirewallRemoveFromResources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    removeFromResourcesRequest := models.RemoveFromResourcesRequest{
        RemoveFrom:            []models.FirewallRemoveFromResources{
            models.FirewallRemoveFromResources{
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
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



