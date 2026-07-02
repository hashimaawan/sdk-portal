# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXR1cw

*This model accepts additional fields of type Object.*


# Class Name

`Status`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`QueryExecutionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/query-execution-state-1.md) | Optional | - |
| `state_change_reason` | `String` | Optional | - |
| `submission_date_time` | `DateTime` | Optional | - |
| `completion_date_time` | `DateTime` | Optional | - |
| `athena_error` | [`AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/athena-error-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
status = Status.new(
  state: QueryExecutionState1::QUEUED,
  state_change_reason: 'StateChangeReason8',
  submission_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  completion_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  athena_error: AthenaError2.new(
    error_category: 3,
    error_type: 128,
    retryable: false,
    error_message: 'ErrorMessage8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



