# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1


# Class Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Prices` | [`[]models.Price6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/price-6.md) | Required | Floating IP type costs per Location |
| `Type` | [`models.Type48Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-48.md) | Required | The type of the Floating IP |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    floatingIp5 := models.FloatingIp5{
        Prices:               []models.Price6{
            models.Price6{
                Location:             "fsn1",
                PriceMonthly:         models.PriceMonthly7{
                    Gross:                "1.1900000000000000",
                    Net:                  "1.0000000000",
                },
            },
        },
        Type:                 models.Type48Enum_IPV4,
    }

}
```



