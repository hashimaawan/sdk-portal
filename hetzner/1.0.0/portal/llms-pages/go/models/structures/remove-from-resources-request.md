# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `RemoveFrom` | [`[]models.FirewallRemoveFromResources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    removeFromResourcesRequest := models.RemoveFromResourcesRequest{
        RemoveFrom:           []models.FirewallRemoveFromResources{
            models.FirewallRemoveFromResources{
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



