# Price 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaWNlNw


# Class Name

`Price7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | `string` | Required | Name of the Location the price is for |
| `PriceHourly` | [`models.PriceHourly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-hourly-6.md) | Required | Hourly costs for a Load Balancer type in this network zone |
| `PriceMonthly` | [`models.PriceMonthly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-monthly-8.md) | Required | Monthly costs for a Load Balancer type in this network zone |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    price7 := models.Price7{
        Location:             "fsn1",
        PriceHourly:          models.PriceHourly6{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
        PriceMonthly:         models.PriceMonthly8{
            Gross:                "1.1900000000000000",
            Net:                  "1.0000000000",
        },
    }

}
```



