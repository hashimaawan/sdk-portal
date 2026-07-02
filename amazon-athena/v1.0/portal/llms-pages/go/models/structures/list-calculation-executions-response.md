# List Calculation Executions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXNwb25zZQ

*This model accepts additional fields of type interface{}.*


# Class Name

`ListCalculationExecutionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `*string` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `Calculations` | [`[]models.CalculationSummary`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/calculation-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |
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
    listCalculationExecutionsResponse := models.ListCalculationExecutionsResponse{
        NextToken:             models.ToPointer("NextToken8"),
        Calculations:          []models.CalculationSummary{
            models.CalculationSummary{
                CalculationExecutionId: models.ToPointer("CalculationExecutionId0"),
                Description:            models.ToPointer("Description2"),
                Status:                 models.ToPointer(models.Status1{
                    SubmissionDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    CompletionDateTime:    models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    State:                 models.ToPointer(models.CalculationExecutionState1_Canceling),
                    StateChangeReason:     models.ToPointer("StateChangeReason8"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:   map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



