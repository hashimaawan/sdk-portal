# Get Query Runtime Statistics Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NPdXRwdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`GetQueryRuntimeStatisticsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryRuntimeStatistics` | [`*models.QueryRuntimeStatistics2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-runtime-statistics-2.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    getQueryRuntimeStatisticsOutput := models.GetQueryRuntimeStatisticsOutput{
        QueryRuntimeStatistics: models.ToPointer(models.QueryRuntimeStatistics2{
            Timeline:              models.ToPointer(models.QueryRuntimeStatisticsTimeline{
                QueryQueueTimeInMillis:        models.ToPointer(156),
                QueryPlanningTimeInMillis:     models.ToPointer(82),
                EngineExecutionTimeInMillis:   models.ToPointer(112),
                ServiceProcessingTimeInMillis: models.ToPointer(126),
                TotalExecutionTimeInMillis:    models.ToPointer(106),
                AdditionalProperties:          map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Rows:                  models.ToPointer(models.QueryRuntimeStatisticsRows{
                InputRows:             models.ToPointer(230),
                InputBytes:            models.ToPointer(250),
                OutputBytes:           models.ToPointer(36),
                OutputRows:            models.ToPointer(230),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            OutputStage:           models.ToPointer(models.OutputStage{
                StageId:               models.ToPointer(130),
                State:                 models.ToPointer("State0"),
                OutputBytes:           models.ToPointer(108),
                OutputRows:            models.ToPointer(158),
                InputBytes:            models.ToPointer(190),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:   map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



