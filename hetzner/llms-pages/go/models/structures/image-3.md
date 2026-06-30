# Image 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkltYWdlMw

The cost of Image per GB/month


# Class Name

`Image3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PricePerGbMonth` | [`models.PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/price-per-gb-month.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    image3 := models.Image3{
        PricePerGbMonth:      models.PricePerGbMonth{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
    }

}
```



