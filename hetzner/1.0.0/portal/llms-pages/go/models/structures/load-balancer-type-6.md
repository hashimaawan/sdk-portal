# Load Balancer Type 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU2


# Class Name

`LoadBalancerType6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `float64` | Required | ID of the Load Balancer type the price is for |
| `Name` | `string` | Required | Name of the Load Balancer type the price is for |
| `Prices` | [`[]models.Price7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-7.md) | Required | Load Balancer type costs per Location |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancerType6 := models.LoadBalancerType6{
        Id:                   float64(1),
        Name:                 "lb11",
        Prices:               []models.Price7{
            models.Price7{
                Location:             "fsn1",
                PriceHourly:          models.PriceHourly6{
                    Gross:                "1.1900000000000000",
                    Net:                  "1.0000000000",
                },
                PriceMonthly:         models.PriceMonthly8{
                    Gross:                "1.1900000000000000",
                    Net:                  "1.0000000000",
                },
            },
        },
    }

}
```



