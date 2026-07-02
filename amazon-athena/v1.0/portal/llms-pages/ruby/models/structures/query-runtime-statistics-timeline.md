# Query Runtime Statistics Timeline

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NUaW1lbGluZQ

Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time.


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


# Example

```ruby
query_runtime_statistics_timeline = QueryRuntimeStatisticsTimeline.new(
  98,
  24,
  54,
  72,
  92
)
```



