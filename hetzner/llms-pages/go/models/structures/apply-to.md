# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkFwcGx5VG8


# Class Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LabelSelector` | [`*models.LabelSelector1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` |
| `Server` | [`*models.Server2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` |
| `Type` | [`models.Type7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-7.md) | Required | Type of the resource |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    applyTo := models.ApplyTo{
        LabelSelector:        models.ToPointer(models.LabelSelector1{
            Selector:             "selector8",
        }),
        Server:               models.ToPointer(models.Server2{
            Id:                   14,
        }),
        Type:                 models.Type7Enum_SERVER,
    }

}
```



