# Get Calculation Execution Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`GetCalculationExecutionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/status-1.md) | Optional | - |
| `statistics` | [`Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/statistics-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_calculation_execution_status_response = GetCalculationExecutionStatusResponse.new(
  status: Status1.new(
    submission_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    completion_date_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    state: CalculationExecutionState1::CANCELING,
    state_change_reason: 'StateChangeReason8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  statistics: Statistics1.new(
    dpu_execution_in_millis: 164,
    progress: 'Progress6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



