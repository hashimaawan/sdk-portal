# Get Calculation Execution Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVzcG9uc2U


# Class Name

`GetCalculationExecutionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/status-1.md) | Optional | - |
| `statistics` | [`Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/statistics-1.md) | Optional | - |


# Example

```ruby
get_calculation_execution_status_response = GetCalculationExecutionStatusResponse.new(
  Status1.new(
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    CalculationExecutionState1Enum::CANCELING,
    'StateChangeReason8'
  ),
  Statistics1.new(
    164,
    'Progress6'
  )
)
```



