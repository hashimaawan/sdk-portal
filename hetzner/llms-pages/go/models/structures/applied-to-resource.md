# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Server` | [`*models.Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/server.md) | Optional | - |
| `Type` | [`*models.Type5Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-5.md) | Optional | Type of resource referenced |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    appliedToResource := models.AppliedToResource{
        Server:               models.ToPointer(models.Server{
            Id:                   14,
        }),
        Type:                 models.ToPointer(models.Type5Enum_SERVER),
    }

}
```



