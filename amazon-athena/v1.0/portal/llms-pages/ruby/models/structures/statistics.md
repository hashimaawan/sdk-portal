# Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXRpc3RpY3M

*This model accepts additional fields of type Object.*


# Class Name

`Statistics`


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
statistics = Statistics.new(
  engine_execution_time_in_millis: 72,
  data_scanned_in_bytes: 60,
  data_manifest_location: 'DataManifestLocation0',
  total_execution_time_in_millis: 146,
  query_queue_time_in_millis: 116,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



