# Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU


# Class Name

`LoadBalancerType`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Deprecated` | `*string` | Required | Point in time when the Load Balancer type is deprecated (in ISO-8601 format) |
| `Description` | `string` | Required | Description of the Load Balancer type |
| `Id` | `float64` | Required | ID of the Load Balancer type |
| `MaxAssignedCertificates` | `float64` | Required | Number of SSL Certificates that can be assigned to a single Load Balancer |
| `MaxConnections` | `float64` | Required | Number of maximum simultaneous open connections |
| `MaxServices` | `float64` | Required | Number of services a Load Balancer of this type can have |
| `MaxTargets` | `float64` | Required | Number of targets a single Load Balancer can have |
| `Name` | `string` | Required | Unique identifier of the Load Balancer type |
| `Prices` | [`[]models.Price`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price.md) | Required | Prices in different network zones |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancerType := models.LoadBalancerType{
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
    }

}
```



