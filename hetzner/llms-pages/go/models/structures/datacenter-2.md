# Datacenter 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkRhdGFjZW50ZXIy

Datacenter this Primary IP is located at


# Class Name

`Datacenter2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `string` | Required | Description of the Datacenter |
| `Id` | `int` | Required | ID of the Resource |
| `Location` | [`models.Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/location.md) | Required | - |
| `Name` | `string` | Required | Unique identifier of the Datacenter |
| `ServerTypes` | [`models.ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/server-types.md) | Required | The Server types the Datacenter can handle |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    datacenter2 := models.Datacenter2{
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
    }

}
```



