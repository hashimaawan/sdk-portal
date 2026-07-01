# Load Balancer Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2U


# Class Name

`LoadBalancerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancerTypes` | [`[]models.LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/load-balancer-type.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancerTypesResponse := models.LoadBalancerTypesResponse{
        LoadBalancerTypes:    []models.LoadBalancerType{
            models.LoadBalancerType{
                Deprecated:              models.ToPointer("2016-01-30T23:50:00+00:00"),
                Description:             "LB11",
                Id:                      float64(1),
                MaxAssignedCertificates: float64(10),
                MaxConnections:          float64(20000),
                MaxServices:             float64(5),
                MaxTargets:              float64(25),
                Name:                    "lb11",
                Prices:                  []models.Price{
                    models.Price{
                        Location:             "fsn1",
                        PriceHourly:          models.PriceHourly{
                            Gross:                "1.1900000000000000",
                            Net:                  "1.0000000000",
                        },
                        PriceMonthly:         models.PriceMonthly{
                            Gross:                "1.1900000000000000",
                            Net:                  "1.0000000000",
                        },
                    },
                },
            },
        },
    }

}
```



