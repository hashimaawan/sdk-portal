# Calculation Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdHVz

Contains information about the status of a notebook calculation.

*This model accepts additional fields of type interface{}.*


# Class Name

`CalculationStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SubmissionDateTime` | `*time.Time` | Optional | - |
| `CompletionDateTime` | `*time.Time` | Optional | - |
| `State` | [`*models.CalculationExecutionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/calculation-execution-state-1.md) | Optional | - |
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
    calculationStatus := models.CalculationStatus{
        SubmissionDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        CompletionDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        State:                 models.ToPointer(models.CalculationExecutionState1_Creating),
        StateChangeReason:     models.ToPointer("StateChangeReason2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



