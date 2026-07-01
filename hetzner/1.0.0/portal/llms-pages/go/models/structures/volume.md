# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlZvbHVtZQ

The cost of Volume per GB/month


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PricePerGbMonth` | [`models.PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-per-gb-month.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    volume := models.Volume{
        PricePerGbMonth:      models.PricePerGbMonth{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
    }

}
```



