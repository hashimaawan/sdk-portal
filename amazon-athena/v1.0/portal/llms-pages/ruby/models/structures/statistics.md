# Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXRpc3RpY3M


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


# Example

```ruby
statistics = Statistics.new(
  72,
  60,
  'DataManifestLocation0',
  146,
  116,
  nil,
  nil,
  ResultReuseInformation2.new
)
```



