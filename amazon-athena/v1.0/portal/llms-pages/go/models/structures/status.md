# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXR1cw


# Class Name

`Status`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `State` | [`*models.QueryExecutionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/query-execution-state-1.md) | Optional | - |
| `StateChangeReason` | `*string` | Optional | - |
| `SubmissionDateTime` | `*time.Time` | Optional | - |
| `CompletionDateTime` | `*time.Time` | Optional | - |
| `AthenaError` | [`*models.AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/athena-error-2.md) | Optional | - |


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
    status := models.Status{
        State:                models.ToPointer(models.QueryExecutionState1Enum_QUEUED),
        StateChangeReason:    models.ToPointer("StateChangeReason8"),
        SubmissionDateTime:   models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        CompletionDateTime:   models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        AthenaError:          models.ToPointer(models.AthenaError2{
            ErrorCategory:        models.ToPointer(3),
            ErrorType:            models.ToPointer(128),
            Retryable:            models.ToPointer(false),
            ErrorMessage:         models.ToPointer("ErrorMessage8"),
        }),
    }

}
```



