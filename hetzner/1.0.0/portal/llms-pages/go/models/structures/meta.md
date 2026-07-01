# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRk1ldGE


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`models.Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/pagination.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    meta := models.Meta{
        Pagination:           models.Pagination{
            LastPage:             models.ToPointer(float64(4)),
            NextPage:             models.ToPointer(float64(4)),
            Page:                 float64(3),
            PerPage:              float64(25),
            PreviousPage:         models.ToPointer(float64(2)),
            TotalEntries:         models.ToPointer(float64(100)),
        },
    }

}
```



