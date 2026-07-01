# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplyTo` | [`[]models.FirewallApplyToResources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    applyToResourcesRequest := models.ApplyToResourcesRequest{
        ApplyTo:              []models.FirewallApplyToResources{
            models.FirewallApplyToResources{
                LabelSelector:        models.ToPointer(models.LabelSelector5{
                    Selector:             "selector8",
                }),
                Server:               models.ToPointer(models.Server9{
                    Id:                   14,
                }),
                Type:                 models.ToPointer(models.Type7Enum_SERVER),
            },
        },
    }

}
```



