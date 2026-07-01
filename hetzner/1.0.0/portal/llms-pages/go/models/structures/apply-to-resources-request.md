# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type interface{}.*


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplyTo` | [`[]models.FirewallApplyToResources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    applyToResourcesRequest := models.ApplyToResourcesRequest{
        ApplyTo:               []models.FirewallApplyToResources{
            models.FirewallApplyToResources{
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



