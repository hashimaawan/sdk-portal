# Datacenters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZTE


# Class Name

`DatacentersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Datacenter` | [`models.Datacenter`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/datacenter.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    datacentersResponse1 := models.DatacentersResponse1{
        Datacenter:           models.Datacenter{
            Description:          "Falkenstein DC Park 8",
            Id:                   42,
            Location:             models.Location{
                City:                 "Falkenstein",
                Country:              "DE",
                Description:          "Falkenstein DC Park 1",
                Id:                   float64(1),
                Latitude:             float64(50.47612),
                Longitude:            float64(12.370071),
                Name:                 "fsn1",
                NetworkZone:          "eu-central",
            },
            Name:                 "fsn1-dc8",
            ServerTypes:          models.ServerTypes{
                Available:             []float64{
                    float64(1),
                    float64(2),
                    float64(3),
                },
                AvailableForMigration: []float64{
                    float64(1),
                    float64(2),
                    float64(3),
                },
                Supported:             []float64{
                    float64(1),
                    float64(2),
                    float64(3),
                },
            },
        },
    }

}
```



