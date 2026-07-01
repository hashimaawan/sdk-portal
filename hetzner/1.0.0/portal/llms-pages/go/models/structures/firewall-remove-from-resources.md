# Firewall Remove from Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVtb3ZlRnJvbVJlc291cmNlcw


# Class Name

`FirewallRemoveFromResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LabelSelector` | [`*models.LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `Server` | [`*models.Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `Type` | [`*models.Type7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-7.md) | Optional | Type of the resource |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    firewallRemoveFromResources := models.FirewallRemoveFromResources{
        LabelSelector:        models.ToPointer(models.LabelSelector5{
            Selector:             "selector8",
        }),
        Server:               models.ToPointer(models.Server9{
            Id:                   14,
        }),
        Type:                 models.ToPointer(models.Type7Enum_SERVER),
    }

}
```



