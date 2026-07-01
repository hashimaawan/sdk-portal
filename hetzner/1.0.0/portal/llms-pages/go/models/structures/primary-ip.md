# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaW1hcnlJcA

*This model accepts additional fields of type interface{}.*


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Prices` | [`[]models.Price8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-8.md) | Required | Primary IP type costs per Location |
| `Type` | [`models.Type49`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-49.md) | Required | The type of the Primary IP |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    primaryIp := models.PrimaryIp{
        Prices:                []models.Price8{
            models.Price8{
                Location:              "fsn1",
                PriceHourly:           models.PriceHourly7{
                    Gross:                 "1.1900000000000000",
                    Net:                   "1.0000000000",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                PriceMonthly:          models.PriceMonthly9{
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
        Type:                  models.Type49_Ipv4,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



