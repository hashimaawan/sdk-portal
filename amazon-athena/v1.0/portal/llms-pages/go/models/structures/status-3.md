# Status 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXR1czM

*This model accepts additional fields of type interface{}.*


# Class Name

`Status3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StartDateTime` | `*time.Time` | Optional | - |
| `LastModifiedDateTime` | `*time.Time` | Optional | - |
| `EndDateTime` | `*time.Time` | Optional | - |
| `IdleSinceDateTime` | `*time.Time` | Optional | - |
| `State` | [`*models.SessionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/session-state-1.md) | Optional | - |
| `StateChangeReason` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "amazonAthena/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    status3 := models.Status3{
        StartDateTime:         models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        LastModifiedDateTime:  models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        EndDateTime:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        IdleSinceDateTime:     models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        State:                 models.ToPointer(models.SessionState1_Creating),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



