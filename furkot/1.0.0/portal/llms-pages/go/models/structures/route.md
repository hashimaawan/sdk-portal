# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop

*This model accepts additional fields of type interface{}.*


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Distance` | `*int64` | Optional | route distance in meters |
| `Duration` | `*int64` | Optional | route duration in seconds |
| `Mode` | [`*models.Mode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/go/models/enumerations/mode.md) | Optional | travel mode |
| `Polyline` | `*string` | Optional | route path compatible with Google polyline encoding algorithm |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "furkotTrips/models"
)

func main() {
    route := models.Route{
        Distance:              models.ToPointer(int64(134)),
        Duration:              models.ToPointer(int64(168)),
        Mode:                  models.ToPointer(models.Mode_Car),
        Polyline:              models.ToPointer("polyline0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



