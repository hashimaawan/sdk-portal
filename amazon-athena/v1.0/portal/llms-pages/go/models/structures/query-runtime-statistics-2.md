# Query Runtime Statistics 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3My


# Class Name

`QueryRuntimeStatistics2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Timeline` | [`*models.QueryRuntimeStatisticsTimeline`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-runtime-statistics-timeline.md) | Optional | Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time. |
| `Rows` | [`*models.QueryRuntimeStatisticsRows`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/query-runtime-statistics-rows.md) | Optional | Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query. |
| `OutputStage` | [`*models.OutputStage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/output-stage.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    queryRuntimeStatistics2 := models.QueryRuntimeStatistics2{
        Timeline:             models.ToPointer(models.QueryRuntimeStatisticsTimeline{
            QueryQueueTimeInMillis:        models.ToPointer(156),
            QueryPlanningTimeInMillis:     models.ToPointer(82),
            EngineExecutionTimeInMillis:   models.ToPointer(112),
            ServiceProcessingTimeInMillis: models.ToPointer(126),
            TotalExecutionTimeInMillis:    models.ToPointer(106),
        }),
        Rows:                 models.ToPointer(models.QueryRuntimeStatisticsRows{
            InputRows:            models.ToPointer(230),
            InputBytes:           models.ToPointer(250),
            OutputBytes:          models.ToPointer(36),
            OutputRows:           models.ToPointer(230),
        }),
        OutputStage:          models.ToPointer(models.OutputStage{
            StageId:              models.ToPointer(130),
            State:                models.ToPointer("State0"),
            OutputBytes:          models.ToPointer(108),
            OutputRows:           models.ToPointer(158),
            InputBytes:           models.ToPointer(190),
        }),
    }

}
```



