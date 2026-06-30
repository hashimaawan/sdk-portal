# Trip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/go/x-redirect/JTI0bSUyRlRyaXA


# Class Name

`Trip`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Begin` | `*time.Time` | Optional | begin of the trip in its local timezone as YYYY-MM-DDThh:mm |
| `Description` | `*string` | Optional | description of the trip (truncated to 200 characters) |
| `End` | `*time.Time` | Optional | end of the trip in its local timezone as YYYY-MM-DDThh:mm |
| `Id` | `*string` | Optional | Unique ID of the trip |
| `Name` | `*string` | Optional | name of the trip |


# Example

```go
package main

import (
    "log"
    "time"
    "furkottrips/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    trip := models.Trip{
        Begin:                models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Description:          models.ToPointer("description8"),
        End:                  models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Id:                   models.ToPointer("id8"),
        Name:                 models.ToPointer("name8"),
    }

}
```



