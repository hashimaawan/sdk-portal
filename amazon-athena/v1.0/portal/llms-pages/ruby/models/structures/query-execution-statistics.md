# Query Execution Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGlzdGljcw

The amount of data scanned during the query execution and the amount of time that it took to execute, and the type of statement that was run.


# Class Name

`QueryExecutionStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `engine_execution_time_in_millis` | `Integer` | Optional | - |
| `data_scanned_in_bytes` | `Integer` | Optional | - |
| `data_manifest_location` | `String` | Optional | - |
| `total_execution_time_in_millis` | `Integer` | Optional | - |
| `query_queue_time_in_millis` | `Integer` | Optional | - |
| `query_planning_time_in_millis` | `Integer` | Optional | - |
| `service_processing_time_in_millis` | `Integer` | Optional | - |
| `result_reuse_information` | [`ResultReuseInformation2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-reuse-information-2.md) | Optional | - |


# Example

```ruby
query_execution_statistics = QueryExecutionStatistics.new(
  68,
  56,
  'DataManifestLocation2',
  106,
  112,
  nil,
  nil,
  ResultReuseInformation2.new
)
```



