# Query Execution Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGlzdGljcw

The amount of data scanned during the query execution and the amount of time that it took to execute, and the type of statement that was run.

*This model accepts additional fields of type Object.*


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
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
query_execution_statistics = QueryExecutionStatistics.new(
  engine_execution_time_in_millis: 68,
  data_scanned_in_bytes: 56,
  data_manifest_location: 'DataManifestLocation2',
  total_execution_time_in_millis: 106,
  query_queue_time_in_millis: 112,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



