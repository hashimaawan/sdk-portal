# Status 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXR1czE

*This model accepts additional fields of type Object.*


# Class Name

`Status1`


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
status1 = Status1.new(
  submission_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  completion_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  state: CalculationExecutionState1::QUEUED,
  state_change_reason: 'StateChangeReason0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



