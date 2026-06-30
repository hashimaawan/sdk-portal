# Firewall Apply to Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkZpcmV3YWxsQXBwbHlUb1Jlc291cmNlcw


# Class Name

`FirewallApplyToResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LabelSelector` | [`*models.LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `Server` | [`*models.Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `Type` | [`*models.Type7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-7.md) | Optional | Type of the resource |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    firewallApplyToResources := models.FirewallApplyToResources{
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



