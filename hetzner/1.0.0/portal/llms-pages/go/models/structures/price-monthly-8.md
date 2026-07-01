# Price Monthly 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTg

Monthly costs for a Load Balancer type in this network zone

*This model accepts additional fields of type interface{}.*


# Class Name

`PriceMonthly8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Gross` | `string` | Required | Price with VAT added |
| `Net` | `string` | Required | Price without VAT |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    priceMonthly8 := models.PriceMonthly8{
        Gross:                 "1.1900000000000000",
        Net:                   "1.0000000000",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



