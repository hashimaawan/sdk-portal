# List Calculation Executions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXNwb25zZQ


# Class Name

`ListCalculationExecutionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `calculations` | [`Array[CalculationSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/calculation-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |


# Example

```ruby
list_calculation_executions_response = ListCalculationExecutionsResponse.new(
  'NextToken2',
  [
    CalculationSummary.new(
      'CalculationExecutionId0',
      'Description2',
      Status1.new(
        DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        CalculationExecutionState1Enum::CANCELING,
        'StateChangeReason8'
      )
    ),
    CalculationSummary.new(
      'CalculationExecutionId0',
      'Description2',
      Status1.new(
        DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
        CalculationExecutionState1Enum::CANCELING,
        'StateChangeReason8'
      )
    )
  ]
)
```



