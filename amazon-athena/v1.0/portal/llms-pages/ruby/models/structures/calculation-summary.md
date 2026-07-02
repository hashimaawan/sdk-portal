# Calculation Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3VtbWFyeQ

Summary information for a notebook calculation.

*This model accepts additional fields of type Object.*


# Class Name

`CalculationSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/status-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
calculation_summary = CalculationSummary.new(
  calculation_execution_id: 'CalculationExecutionId2',
  description: 'Description4',
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
```



