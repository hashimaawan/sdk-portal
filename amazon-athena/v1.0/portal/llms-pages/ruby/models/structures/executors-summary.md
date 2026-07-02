# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.

*This model accepts additional fields of type Object.*


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `executor_id` | `String` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` |
| `executor_type` | [`ExecutorType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/executor-type-2.md) | Optional | - |
| `start_date_time` | `Integer` | Optional | - |
| `termination_date_time` | `Integer` | Optional | - |
| `executor_state` | [`ExecutorState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/executor-state-3.md) | Optional | - |
| `executor_size` | `Integer` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
executors_summary = ExecutorsSummary.new(
  executor_id: 'ExecutorId2',
  executor_type: ExecutorType2::GATEWAY,
  start_date_time: 204,
  termination_date_time: 160,
  executor_state: ExecutorState3::CREATING,
  executor_size: 118,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



