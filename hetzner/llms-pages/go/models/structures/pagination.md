# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlBhZ2luYXRpb24


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LastPage` | `*float64` | Required | ID of the last page available. Can be null if the current page is the last one. |
| `NextPage` | `*float64` | Required | ID of the next page. Can be null if the current page is the last one. |
| `Page` | `float64` | Required | Current page number |
| `PerPage` | `float64` | Required | Maximum number of items shown per page in the response |
| `PreviousPage` | `*float64` | Required | ID of the previous page. Can be null if the current page is the first one. |
| `TotalEntries` | `*float64` | Required | The total number of entries that exist in the database for this query. Nullable if unknown. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    pagination := models.Pagination{
        LastPage:             models.ToPointer(float64(4)),
        NextPage:             models.ToPointer(float64(4)),
        Page:                 float64(3),
        PerPage:              float64(25),
        PreviousPage:         models.ToPointer(float64(2)),
        TotalEntries:         models.ToPointer(float64(100)),
    }

}
```



