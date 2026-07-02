# Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXRpc3RpY3M


# Class Name

`Statistics`


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


# Example

```python
from amazonathena.models.statistics import Statistics

statistics = Statistics(
    engine_execution_time_in_millis=72,
    data_scanned_in_bytes=60,
    data_manifest_location='DataManifestLocation0',
    total_execution_time_in_millis=146,
    query_queue_time_in_millis=116
)
```



