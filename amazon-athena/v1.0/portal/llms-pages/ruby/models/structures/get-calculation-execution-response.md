# Get Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uUmVzcG9uc2U

*This model accepts additional fields of type Object.*


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
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_calculation_execution_response = GetCalculationExecutionResponse.new(
  calculation_execution_id: 'CalculationExecutionId2',
  session_id: 'SessionId6',
  description: 'Description4',
  working_directory: 'WorkingDirectory0',
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



