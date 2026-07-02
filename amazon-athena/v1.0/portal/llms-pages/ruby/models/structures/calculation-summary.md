# Calculation Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3VtbWFyeQ

Summary information for a notebook calculation.


# Class Name

`CalculationSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/status-1.md) | Optional | - |


# Example

```ruby
calculation_summary = CalculationSummary.new(
  'CalculationExecutionId2',
  'Description4',
  Status1.new(
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    CalculationExecutionState1Enum::CANCELING,
    'StateChangeReason8'
  )
)
```



