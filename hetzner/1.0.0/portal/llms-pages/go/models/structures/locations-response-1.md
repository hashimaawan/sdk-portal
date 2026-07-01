# Locations Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type interface{}.*


# Class Name

`LocationsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Location` | [`models.Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/location.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    locationsResponse1 := models.LocationsResponse1{
        Location:              models.Location{
            City:                  "Falkenstein",
            Country:               "DE",
            Description:           "Falkenstein DC Park 1",
            Id:                    float64(1),
            Latitude:              float64(50.47612),
            Longitude:             float64(12.370071),
            Name:                  "fsn1",
            NetworkZone:           "eu-central",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



