# Query Runtime Statistics Timeline

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NUaW1lbGluZQ

Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time.

*This model accepts additional fields of type Any.*


# Class Name

`QueryRuntimeStatisticsTimeline`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_queue_time_in_millis` | `int` | Optional | - |
| `query_planning_time_in_millis` | `int` | Optional | - |
| `engine_execution_time_in_millis` | `int` | Optional | - |
| `service_processing_time_in_millis` | `int` | Optional | - |
| `total_execution_time_in_millis` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.query_runtime_statistics_timeline import QueryRuntimeStatisticsTimeline

query_runtime_statistics_timeline = QueryRuntimeStatisticsTimeline(
    query_queue_time_in_millis=98,
    query_planning_time_in_millis=24,
    engine_execution_time_in_millis=54,
    service_processing_time_in_millis=72,
    total_execution_time_in_millis=92,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



