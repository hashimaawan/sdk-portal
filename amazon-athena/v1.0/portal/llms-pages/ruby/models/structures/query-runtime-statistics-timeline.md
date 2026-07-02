# Query Runtime Statistics Timeline

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NUaW1lbGluZQ

Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time.

*This model accepts additional fields of type Object.*


# Class Name

`QueryRuntimeStatisticsTimeline`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_queue_time_in_millis` | `Integer` | Optional | - |
| `query_planning_time_in_millis` | `Integer` | Optional | - |
| `engine_execution_time_in_millis` | `Integer` | Optional | - |
| `service_processing_time_in_millis` | `Integer` | Optional | - |
| `total_execution_time_in_millis` | `Integer` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
query_runtime_statistics_timeline = QueryRuntimeStatisticsTimeline.new(
  query_queue_time_in_millis: 98,
  query_planning_time_in_millis: 24,
  engine_execution_time_in_millis: 54,
  service_processing_time_in_millis: 72,
  total_execution_time_in_millis: 92,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



