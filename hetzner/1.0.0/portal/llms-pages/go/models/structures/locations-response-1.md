# Locations Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2Ux


# Class Name

`LocationsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | [`models.Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/location.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    locationsResponse1 := models.LocationsResponse1{
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
    }

}
```



