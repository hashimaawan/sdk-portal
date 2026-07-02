# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXR1cw


# Class Name

`Status`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`QueryExecutionState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/query-execution-state-1.md) | Optional | - |
| `state_change_reason` | `String` | Optional | - |
| `submission_date_time` | `DateTime` | Optional | - |
| `completion_date_time` | `DateTime` | Optional | - |
| `athena_error` | [`AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/athena-error-2.md) | Optional | - |


# Example

```ruby
status = Status.new(
  QueryExecutionState1Enum::QUEUED,
  'StateChangeReason8',
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  AthenaError2.new(
    3,
    128,
    false,
    'ErrorMessage8'
  )
)
```



