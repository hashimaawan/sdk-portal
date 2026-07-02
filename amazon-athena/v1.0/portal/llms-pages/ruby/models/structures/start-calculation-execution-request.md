# Start Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`StartCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `calculation_configuration` | [`GetCalculationExecutionCodeResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/get-calculation-execution-code-response.md) | Optional | - |
| `code_block` | `String` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `client_request_token` | `String` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
start_calculation_execution_request = StartCalculationExecutionRequest.new(
  session_id: 'SessionId8',
  description: 'Description6',
  calculation_configuration: GetCalculationExecutionCodeResponse.new(
    code_block: 'CodeBlock4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  code_block: 'CodeBlock2',
  client_request_token: 'ClientRequestToken4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



