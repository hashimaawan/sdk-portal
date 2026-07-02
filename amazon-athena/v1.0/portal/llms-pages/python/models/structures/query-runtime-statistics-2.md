# Query Runtime Statistics 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3My

*This model accepts additional fields of type Any.*


# Class Name

`QueryRuntimeStatistics2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `timeline` | [`QueryRuntimeStatisticsTimeline`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-runtime-statistics-timeline.md) | Optional | Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time. |
| `rows` | [`QueryRuntimeStatisticsRows`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-runtime-statistics-rows.md) | Optional | Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query. |
| `output_stage` | [`OutputStage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/output-stage.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.output_stage import OutputStage
from amazonathena.models.query_runtime_statistics_2 import QueryRuntimeStatistics2
from amazonathena.models.query_runtime_statistics_rows import QueryRuntimeStatisticsRows
from amazonathena.models.query_runtime_statistics_timeline import QueryRuntimeStatisticsTimeline

query_runtime_statistics_2 = QueryRuntimeStatistics2(
    timeline=QueryRuntimeStatisticsTimeline(
        query_queue_time_in_millis=156,
        query_planning_time_in_millis=82,
        engine_execution_time_in_millis=112,
        service_processing_time_in_millis=126,
        total_execution_time_in_millis=106,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    rows=QueryRuntimeStatisticsRows(
        input_rows=230,
        input_bytes=250,
        output_bytes=36,
        output_rows=230,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    output_stage=OutputStage(
        stage_id=130,
        state='State0',
        output_bytes=108,
        output_rows=158,
        input_bytes=190,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



