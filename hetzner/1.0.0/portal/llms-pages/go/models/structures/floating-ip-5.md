# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1

*This model accepts additional fields of type interface{}.*


# Class Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Prices` | [`[]models.Price6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-6.md) | Required | Floating IP type costs per Location |
| `Type` | [`models.Type48`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-48.md) | Required | The type of the Floating IP |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    floatingIp5 := models.FloatingIp5{
        Prices:                []models.Price6{
            models.Price6{
                Location:              "fsn1",
                PriceMonthly:          models.PriceMonthly7{
                    Gross:                 "1.1900000000000000",
                    Net:                   "1.0000000000",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Type:                  models.Type48_Ipv4,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



