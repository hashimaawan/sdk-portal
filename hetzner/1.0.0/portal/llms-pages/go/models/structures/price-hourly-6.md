# Price Hourly 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaWNlSG91cmx5Ng

Hourly costs for a Load Balancer type in this network zone


# Class Name

`PriceHourly6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Gross` | `string` | Required | Price with VAT added |
| `Net` | `string` | Required | Price without VAT |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    priceHourly6 := models.PriceHourly6{
        Gross:                "1.1900000000000000",
        Net:                  "1.0000000000",
    }

}
```



