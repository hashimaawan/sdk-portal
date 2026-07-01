# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFwcGxpZWRUbw


# Class Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AppliedToResources` | [`[]models.AppliedToResource`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/applied-to-resource.md) | Optional | - |
| `LabelSelector` | [`*models.LabelSelector`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/label-selector.md) | Optional | - |
| `Server` | [`*models.Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server.md) | Optional | - |
| `Type` | [`models.Type6Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-6.md) | Required | Type of resource referenced |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    appliedTo := models.AppliedTo{
        AppliedToResources:   []models.AppliedToResource{
            models.AppliedToResource{
                Server:               models.ToPointer(models.Server{
                    Id:                   14,
                }),
                Type:                 models.ToPointer(models.Type5Enum_SERVER),
            },
            models.AppliedToResource{
                Server:               models.ToPointer(models.Server{
                    Id:                   14,
                }),
                Type:                 models.ToPointer(models.Type5Enum_SERVER),
            },
        },
        LabelSelector:        models.ToPointer(models.LabelSelector{
            Selector:             "selector8",
        }),
        Server:               models.ToPointer(models.Server{
            Id:                   14,
        }),
        Type:                 models.Type6Enum_SERVER,
    }

}
```



