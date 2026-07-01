# Step

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlN0ZXA

*This model accepts additional fields of type interface{}.*


# Class Name

`Step`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Address` | `*string` | Optional | address of the stop |
| `Arrival` | `*time.Time` | Optional | arrival at the stop in its local timezone as YYYY-MM-DDThh:mm |
| `Coordinates` | [`*models.Coordinates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/go/models/structures/coordinates.md) | Optional | geographical coordinates of the stop |
| `Departure` | `*time.Time` | Optional | departure from the stop in its local timezone as YYYY-MM-DDThh:mm |
| `Name` | `*string` | Optional | name of the stop |
| `Nights` | `*int64` | Optional | number of nights |
| `Passthru` | `*bool` | Optional | true for pass-through points anchoring route |
| `Route` | [`*models.Route`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/go/models/structures/route.md) | Optional | route leading to the stop |
| `Url` | `*string` | Optional | url of the page with more information about the stop |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "furkotTrips/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    step := models.Step{
        Address:               models.ToPointer("address4"),
        Arrival:               models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Coordinates:           models.ToPointer(models.Coordinates{
            Lat:                   models.ToPointer(float64(182.98)),
            Lon:                   models.ToPointer(float64(16.08)),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Departure:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Name:                  models.ToPointer("name8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



