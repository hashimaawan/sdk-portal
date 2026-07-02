# Get Calculation Execution Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`GetCalculationExecutionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Status` | [`*models.Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/status-1.md) | Optional | - |
| `Statistics` | [`*models.Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/statistics-1.md) | Optional | - |
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
    getCalculationExecutionStatusResponse := models.GetCalculationExecutionStatusResponse{
        Status:                models.ToPointer(models.Status1{
            SubmissionDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            CompletionDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            State:                 models.ToPointer(models.CalculationExecutionState1_Canceling),
            StateChangeReason:     models.ToPointer("StateChangeReason8"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Statistics:            models.ToPointer(models.Statistics1{
            DpuExecutionInMillis:  models.ToPointer(164),
            Progress:              models.ToPointer("Progress6"),
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



