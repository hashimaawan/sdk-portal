# Price 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlByaWNlOA


# Class Name

`Price8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceHourly` | [`models.PriceHourly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/price-hourly-7.md) | Required | Hourly costs for a Primary IP type in this Location |
| `PriceMonthly` | [`models.PriceMonthly9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/price-monthly-9.md) | Required | Monthly costs for a Primary IP type in this Location |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    price8 := models.Price8{
        Location:             "fsn1",
        PriceHourly:          models.PriceHourly7{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
        PriceMonthly:         models.PriceMonthly9{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
    }

}
```



