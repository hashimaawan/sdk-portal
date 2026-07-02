# Get Query Runtime Statistics Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NPdXRwdXQ


# Class Name

`GetQueryRuntimeStatisticsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_runtime_statistics` | [`QueryRuntimeStatistics2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-runtime-statistics-2.md) | Optional | - |


# Example

```python
from amazonathena.models.get_query_runtime_statistics_output import GetQueryRuntimeStatisticsOutput
from amazonathena.models.output_stage import OutputStage
from amazonathena.models.query_runtime_statistics_2 import QueryRuntimeStatistics2
from amazonathena.models.query_runtime_statistics_rows import QueryRuntimeStatisticsRows
from amazonathena.models.query_runtime_statistics_timeline import QueryRuntimeStatisticsTimeline

get_query_runtime_statistics_output = GetQueryRuntimeStatisticsOutput(
    query_runtime_statistics=QueryRuntimeStatistics2(
        timeline=QueryRuntimeStatisticsTimeline(
            query_queue_time_in_millis=156,
            query_planning_time_in_millis=82,
            engine_execution_time_in_millis=112,
            service_processing_time_in_millis=126,
            total_execution_time_in_millis=106
        ),
        rows=QueryRuntimeStatisticsRows(
            input_rows=230,
            input_bytes=250,
            output_bytes=36,
            output_rows=230
        ),
        output_stage=OutputStage(
            stage_id=130,
            state='State0',
            output_bytes=108,
            output_rows=158,
            input_bytes=190
        )
    )
)
```



