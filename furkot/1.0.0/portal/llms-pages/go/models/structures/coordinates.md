# Coordinates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNvb3JkaW5hdGVz

geographical coordinates of the stop


# Class Name

`Coordinates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Lat` | `*float64` | Optional | latitude |
| `Lon` | `*float64` | Optional | longitude |


# Example

```go
package main

import (
    "furkottrips/models"
)

func main() {
    coordinates := models.Coordinates{
        Lat:                  models.ToPointer(float64(182.98)),
        Lon:                  models.ToPointer(float64(16.08)),
    }

}
```



