# Price Monthly 10

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTEw

Monthly costs for a Server type in this Location


# Class Name

`PriceMonthly10`


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
    priceMonthly10 := models.PriceMonthly10{
        Gross:                "1.1900000000000000",
        Net:                  "1.0000000000",
    }

}
```



