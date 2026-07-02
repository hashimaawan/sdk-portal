# Query Runtime Statistics Timeline

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NUaW1lbGluZQ

Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time.


# Class Name

`QueryRuntimeStatisticsTimeline`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryQueueTimeInMillis` | `int?` | Optional | - |
| `QueryPlanningTimeInMillis` | `int?` | Optional | - |
| `EngineExecutionTimeInMillis` | `int?` | Optional | - |
| `ServiceProcessingTimeInMillis` | `int?` | Optional | - |
| `TotalExecutionTimeInMillis` | `int?` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

QueryRuntimeStatisticsTimeline queryRuntimeStatisticsTimeline = new QueryRuntimeStatisticsTimeline
{
    QueryQueueTimeInMillis = 122,
    QueryPlanningTimeInMillis = 48,
    EngineExecutionTimeInMillis = 78,
    ServiceProcessingTimeInMillis = 96,
    TotalExecutionTimeInMillis = 140,
};
```



