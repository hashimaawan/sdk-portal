# Calculation Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdHVz

Contains information about the status of a notebook calculation.

*This model accepts additional fields of type Object.*


# Class Name

`CalculationStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `submission_date_time` | `DateTime` | Optional | - |
| `completion_date_time` | `DateTime` | Optional | - |
| `state` | [`CalculationExecutionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/calculation-execution-state-1.md) | Optional | - |
| `state_change_reason` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
calculation_status = CalculationStatus.new(
  submission_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  completion_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  state: CalculationExecutionState1::CREATING,
  state_change_reason: 'StateChangeReason4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



