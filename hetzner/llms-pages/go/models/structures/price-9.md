# Price 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlByaWNlOQ


# Class Name

`Price9`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceHourly` | [`models.PriceHourly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/price-hourly-8.md) | Required | Hourly costs for a Server type in this Location |
| `PriceMonthly` | [`models.PriceMonthly10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/price-monthly-10.md) | Required | Monthly costs for a Server type in this Location |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    price9 := models.Price9{
        Location:             "fsn1",
        PriceHourly:          models.PriceHourly8{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
        PriceMonthly:         models.PriceMonthly10{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
    }

}
```



