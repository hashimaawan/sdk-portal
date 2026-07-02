# Query Execution Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGlzdGljcw

The amount of data scanned during the query execution and the amount of time that it took to execute, and the type of statement that was run.

*This model accepts additional fields of type Any.*


# Class Name

`QueryExecutionStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `engine_execution_time_in_millis` | `int` | Optional | - |
| `data_scanned_in_bytes` | `int` | Optional | - |
| `data_manifest_location` | `str` | Optional | - |
| `total_execution_time_in_millis` | `int` | Optional | - |
| `query_queue_time_in_millis` | `int` | Optional | - |
| `query_planning_time_in_millis` | `int` | Optional | - |
| `service_processing_time_in_millis` | `int` | Optional | - |
| `result_reuse_information` | [`ResultReuseInformation2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result-reuse-information-2.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.query_execution_statistics import QueryExecutionStatistics

query_execution_statistics = QueryExecutionStatistics(
    engine_execution_time_in_millis=68,
    data_scanned_in_bytes=56,
    data_manifest_location='DataManifestLocation2',
    total_execution_time_in_millis=106,
    query_queue_time_in_millis=112,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



