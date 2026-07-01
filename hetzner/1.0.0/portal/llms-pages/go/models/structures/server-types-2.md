# Server Types 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzMg

*This model accepts additional fields of type interface{}.*


# Class Name

`ServerTypes2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `float64` | Required | ID of the Server type the price is for |
| `Name` | `string` | Required | Name of the Server type the price is for |
| `Prices` | [`[]models.Price9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-9.md) | Required | Server type costs per Location |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serverTypes2 := models.ServerTypes2{
        Id:                    float64(4),
        Name:                  "cx11",
        Prices:                []models.Price9{
            models.Price9{
                Location:              "fsn1",
                PriceHourly:           models.PriceHourly8{
                    Gross:                 "1.1900000000000000",
                    Net:                   "1.0000000000",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                PriceMonthly:          models.PriceMonthly10{
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
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



