# Coordinates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNvb3JkaW5hdGVz

geographical coordinates of the stop

*This model accepts additional fields of type interface{}.*


# Class Name

`Coordinates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Lat` | `*float64` | Optional | latitude |
| `Lon` | `*float64` | Optional | longitude |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "furkotTrips/models"
)

func main() {
    coordinates := models.Coordinates{
        Lat:                   models.ToPointer(float64(182.98)),
        Lon:                   models.ToPointer(float64(16.08)),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



