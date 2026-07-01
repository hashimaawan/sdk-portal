# Price 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaWNlNg


# Class Name

`Price6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceMonthly` | [`models.PriceMonthly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-monthly-7.md) | Required | Monthly costs for a Floating IP type in this Location |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    price6 := models.Price6{
        Location:             "fsn1",
        PriceMonthly:         models.PriceMonthly7{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
    }

}
```



