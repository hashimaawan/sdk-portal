# Location 16

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvY2F0aW9uMTY

Location of the Volume. Volume can only be attached to Servers in the same Location.

*This model accepts additional fields of type interface{}.*


# Class Name

`Location16`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `City` | `string` | Required | City the Location is closest to |
| `Country` | `string` | Required | ISO 3166-1 alpha-2 code of the country the Location resides in |
| `Description` | `string` | Required | Description of the Location |
| `Id` | `float64` | Required | ID of the Location |
| `Latitude` | `float64` | Required | Latitude of the city closest to the Location |
| `Longitude` | `float64` | Required | Longitude of the city closest to the Location |
| `Name` | `string` | Required | Unique identifier of the Location |
| `NetworkZone` | `string` | Required | Name of network zone this Location resides in |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    location16 := models.Location16{
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
    }

}
```



