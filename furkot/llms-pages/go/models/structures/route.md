# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/go/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Distance` | `*int64` | Optional | route distance in meters |
| `Duration` | `*int64` | Optional | route duration in seconds |
| `Mode` | [`*models.ModeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/go/models/enumerations/mode.md) | Optional | travel mode |
| `Polyline` | `*string` | Optional | route path compatible with Google polyline encoding algorithm |


# Example

```go
package main

import (
    "furkottrips/models"
)

func main() {
    route := models.Route{
        Distance:             models.ToPointer(int64(134)),
        Duration:             models.ToPointer(int64(168)),
        Mode:                 models.ToPointer(models.ModeEnum_CAR),
        Polyline:             models.ToPointer("polyline0"),
    }

}
```



