# Get Query Runtime Statistics Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NPdXRwdXQ


# Class Name

`GetQueryRuntimeStatisticsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryRuntimeStatistics` | [`QueryRuntimeStatistics2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-runtime-statistics-2.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

GetQueryRuntimeStatisticsOutput getQueryRuntimeStatisticsOutput = new GetQueryRuntimeStatisticsOutput
{
    QueryRuntimeStatistics = new QueryRuntimeStatistics2
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
    },
};
```



