# Price Monthly 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTY


# Class Name

`PriceMonthly6`


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
    priceMonthly6 := models.PriceMonthly6{
        Gross:                "1.1900000000000000",
        Net:                  "1.0000000000",
    }

}
```



