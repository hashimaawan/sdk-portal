# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `executor_id` | `String` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` |
| `executor_type` | [`ExecutorType2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/executor-type-2.md) | Optional | - |
| `start_date_time` | `Integer` | Optional | - |
| `termination_date_time` | `Integer` | Optional | - |
| `executor_state` | [`ExecutorState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/executor-state-3.md) | Optional | - |
| `executor_size` | `Integer` | Optional | - |


# Example

```ruby
executors_summary = ExecutorsSummary.new(
  'ExecutorId2',
  ExecutorType2Enum::GATEWAY,
  204,
  160,
  ExecutorState3Enum::CREATING,
  118
)
```



