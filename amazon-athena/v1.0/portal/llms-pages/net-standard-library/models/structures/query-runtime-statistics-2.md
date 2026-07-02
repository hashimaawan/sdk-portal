# Query Runtime Statistics 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3My


# Class Name

`QueryRuntimeStatistics2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Timeline` | [`QueryRuntimeStatisticsTimeline`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-runtime-statistics-timeline.md) | Optional | Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time. |
| `Rows` | [`QueryRuntimeStatisticsRows`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-runtime-statistics-rows.md) | Optional | Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query. |
| `OutputStage` | [`OutputStage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/output-stage.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

QueryRuntimeStatistics2 queryRuntimeStatistics2 = new QueryRuntimeStatistics2
{
    Timeline = new QueryRuntimeStatisticsTimeline
    {
        QueryQueueTimeInMillis = 156,
        QueryPlanningTimeInMillis = 82,
        EngineExecutionTimeInMillis = 112,
        ServiceProcessingTimeInMillis = 126,
        TotalExecutionTimeInMillis = 106,
    },
    Rows = new QueryRuntimeStatisticsRows
    {
        InputRows = 230,
        InputBytes = 250,
        OutputBytes = 36,
        OutputRows = 230,
    },
    OutputStage = new OutputStage
    {
        StageId = 130,
        State = "State0",
        OutputBytes = 108,
        OutputRows = 158,
        InputBytes = 190,
    },
};
```



