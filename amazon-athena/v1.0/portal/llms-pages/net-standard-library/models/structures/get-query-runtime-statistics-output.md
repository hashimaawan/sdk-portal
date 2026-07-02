# Get Query Runtime Statistics Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NPdXRwdXQ

*This model accepts additional fields of type object.*


# Class Name

`GetQueryRuntimeStatisticsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryRuntimeStatistics` | [`QueryRuntimeStatistics2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/query-runtime-statistics-2.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Rows = new QueryRuntimeStatisticsRows
        {
            InputRows = 230,
            InputBytes = 250,
            OutputBytes = 36,
            OutputRows = 230,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        OutputStage = new OutputStage
        {
            StageId = 130,
            State = "State0",
            OutputBytes = 108,
            OutputRows = 158,
            InputBytes = 190,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



