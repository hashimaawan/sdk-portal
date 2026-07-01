# Price Monthly 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTk

Monthly costs for a Primary IP type in this Location


# Class Name

`PriceMonthly9`


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
    priceMonthly9 := models.PriceMonthly9{
        Gross:                "1.1900000000000000",
        Net:                  "1.0000000000",
    }

}
```



