# Get Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uUmVzcG9uc2U


# Class Name

`GetCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `session_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `working_directory` | `String` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/status-1.md) | Optional | - |
| `statistics` | [`Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/statistics-1.md) | Optional | - |
| `result` | [`Result`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result.md) | Optional | - |


# Example

```ruby
get_calculation_execution_response = GetCalculationExecutionResponse.new(
  'CalculationExecutionId2',
  'SessionId6',
  'Description4',
  'WorkingDirectory0',
  Status1.new(
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    CalculationExecutionState1Enum::CANCELING,
    'StateChangeReason8'
  ),
  Statistics1.new,
  Result.new
)
```



