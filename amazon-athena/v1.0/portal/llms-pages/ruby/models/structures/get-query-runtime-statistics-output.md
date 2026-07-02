# Get Query Runtime Statistics Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`GetQueryRuntimeStatisticsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_runtime_statistics` | [`QueryRuntimeStatistics2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-runtime-statistics-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_query_runtime_statistics_output = GetQueryRuntimeStatisticsOutput.new(
  query_runtime_statistics: QueryRuntimeStatistics2.new(
    timeline: QueryRuntimeStatisticsTimeline.new(
      query_queue_time_in_millis: 156,
      query_planning_time_in_millis: 82,
      engine_execution_time_in_millis: 112,
      service_processing_time_in_millis: 126,
      total_execution_time_in_millis: 106,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    rows: QueryRuntimeStatisticsRows.new(
      input_rows: 230,
      input_bytes: 250,
      output_bytes: 36,
      output_rows: 230,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    output_stage: OutputStage.new(
      stage_id: 130,
      state: 'State0',
      output_bytes: 108,
      output_rows: 158,
      input_bytes: 190,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



