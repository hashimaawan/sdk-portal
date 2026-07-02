# Query Runtime Statistics Timeline

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NUaW1lbGluZQ

Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time.


# Class Name

`QueryRuntimeStatisticsTimeline`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryQueueTimeInMillis` | `*int` | Optional | - |
| `QueryPlanningTimeInMillis` | `*int` | Optional | - |
| `EngineExecutionTimeInMillis` | `*int` | Optional | - |
| `ServiceProcessingTimeInMillis` | `*int` | Optional | - |
| `TotalExecutionTimeInMillis` | `*int` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    queryRuntimeStatisticsTimeline := models.QueryRuntimeStatisticsTimeline{
        QueryQueueTimeInMillis:        models.ToPointer(122),
        QueryPlanningTimeInMillis:     models.ToPointer(48),
        EngineExecutionTimeInMillis:   models.ToPointer(78),
        ServiceProcessingTimeInMillis: models.ToPointer(96),
        TotalExecutionTimeInMillis:    models.ToPointer(140),
    }

}
```



