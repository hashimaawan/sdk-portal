# List Calculation Executions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`ListCalculationExecutionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `calculations` | [`Array[CalculationSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/calculation-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_calculation_executions_response = ListCalculationExecutionsResponse.new(
  next_token: 'NextToken2',
  calculations: [
    CalculationSummary.new(
      calculation_execution_id: 'CalculationExecutionId0',
      description: 'Description2',
      status: Status1.new(
        submission_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        completion_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        state: CalculationExecutionState1::CANCELING,
        state_change_reason: 'StateChangeReason8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    CalculationSummary.new(
      calculation_execution_id: 'CalculationExecutionId0',
      description: 'Description2',
      status: Status1.new(
        submission_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        completion_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        state: CalculationExecutionState1::CANCELING,
        state_change_reason: 'StateChangeReason8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



