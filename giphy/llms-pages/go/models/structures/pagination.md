# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/go/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions.


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Count` | `*int` | Optional | Total number of items returned. |
| `Offset` | `*int` | Optional | Position in pagination. |
| `TotalCount` | `*int` | Optional | Total number of items available. |


# Example

```go
package main

import (
    "giphyapi/models"
)

func main() {
    pagination := models.Pagination{
        Count:                models.ToPointer(25),
        Offset:               models.ToPointer(75),
        TotalCount:           models.ToPointer(250),
    }

}
```



