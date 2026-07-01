# Price

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaWNl


# Class Name

`Price`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceHourly` | [`models.PriceHourly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-hourly.md) | Required | Hourly costs for a Resource in this Location |
| `PriceMonthly` | [`models.PriceMonthly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-monthly.md) | Required | Monthly costs for a Resource in this Location |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    price := models.Price{
        Location:             "fsn1",
        PriceHourly:          models.PriceHourly{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
        PriceMonthly:         models.PriceMonthly{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
    }

}
```



