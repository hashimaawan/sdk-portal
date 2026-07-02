# Status 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXR1czE


# Class Name

`Status1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SubmissionDateTime` | `*time.Time` | Optional | - |
| `CompletionDateTime` | `*time.Time` | Optional | - |
| `State` | [`*models.CalculationExecutionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/calculation-execution-state-1.md) | Optional | - |
| `StateChangeReason` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "log"
    "time"
    "amazonathena/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    status1 := models.Status1{
        SubmissionDateTime:   models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        CompletionDateTime:   models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        State:                models.ToPointer(models.CalculationExecutionState1Enum_QUEUED),
        StateChangeReason:    models.ToPointer("StateChangeReason0"),
    }

}
```



