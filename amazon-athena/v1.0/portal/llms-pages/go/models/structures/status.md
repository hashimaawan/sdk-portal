# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXR1cw

*This model accepts additional fields of type interface{}.*


# Class Name

`Status`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `State` | [`*models.QueryExecutionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/query-execution-state-1.md) | Optional | - |
| `StateChangeReason` | `*string` | Optional | - |
| `SubmissionDateTime` | `*time.Time` | Optional | - |
| `CompletionDateTime` | `*time.Time` | Optional | - |
| `AthenaError` | [`*models.AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/athena-error-2.md) | Optional | - |
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
    status := models.Status{
        State:                 models.ToPointer(models.QueryExecutionState1_Queued),
        StateChangeReason:     models.ToPointer("StateChangeReason8"),
        SubmissionDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        CompletionDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        AthenaError:           models.ToPointer(models.AthenaError2{
            ErrorCategory:         models.ToPointer(3),
            ErrorType:             models.ToPointer(128),
            Retryable:             models.ToPointer(false),
            ErrorMessage:          models.ToPointer("ErrorMessage8"),
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



