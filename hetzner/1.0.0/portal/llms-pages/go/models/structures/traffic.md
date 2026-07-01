# Traffic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlRyYWZmaWM

The cost of additional traffic per TB


# Class Name

`Traffic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PricePerTb` | [`models.PricePerTb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-per-tb.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    traffic := models.Traffic{
        PricePerTb:           models.PricePerTb{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
    }

}
```



