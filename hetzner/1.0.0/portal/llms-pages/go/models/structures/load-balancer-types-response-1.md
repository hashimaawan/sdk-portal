# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancerType` | [`*models.LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/load-balancer-type.md) | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancerTypesResponse1 := models.LoadBalancerTypesResponse1{
        LoadBalancerType:     models.ToPointer(models.LoadBalancerType{
            Deprecated:              models.ToPointer("deprecated2"),
            Description:             "description4",
            Id:                      float64(205.06),
            MaxAssignedCertificates: float64(211.64),
            MaxConnections:          float64(136.32),
            MaxServices:             float64(199.18),
            MaxTargets:              float64(152.52),
            Name:                    "name6",
            Prices:                  []models.Price{
                models.Price{
                    Location:             "location8",
                    PriceHourly:          models.PriceHourly{
                        Gross:                "gross4",
                        Net:                  "net2",
                    },
                    PriceMonthly:         models.PriceMonthly{
                        Gross:                "gross2",
                        Net:                  "net0",
                    },
                },
                models.Price{
                    Location:             "location8",
                    PriceHourly:          models.PriceHourly{
                        Gross:                "gross4",
                        Net:                  "net2",
                    },
                    PriceMonthly:         models.PriceMonthly{
                        Gross:                "gross2",
                        Net:                  "net0",
                    },
                },
                models.Price{
                    Location:             "location8",
                    PriceHourly:          models.PriceHourly{
                        Gross:                "gross4",
                        Net:                  "net2",
                    },
                    PriceMonthly:         models.PriceMonthly{
                        Gross:                "gross2",
                        Net:                  "net0",
                    },
                },
            },
        }),
    }

}
```



