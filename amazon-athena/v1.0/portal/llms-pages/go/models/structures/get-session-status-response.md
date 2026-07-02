# Get Session Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFNlc3Npb25TdGF0dXNSZXNwb25zZQ

*This model accepts additional fields of type interface{}.*


# Class Name

`GetSessionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Status` | [`*models.Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/status-3.md) | Optional | - |
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
    getSessionStatusResponse := models.GetSessionStatusResponse{
        SessionId:             models.ToPointer("SessionId4"),
        Status:                models.ToPointer(models.Status3{
            StartDateTime:         models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            LastModifiedDateTime:  models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            EndDateTime:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            IdleSinceDateTime:     models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            State:                 models.ToPointer(models.SessionState1_Terminating),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



