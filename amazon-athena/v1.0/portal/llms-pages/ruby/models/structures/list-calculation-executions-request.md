# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `state_filter` | [`CalculationExecutionState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/calculation-execution-state-3.md) | Optional | - |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `String` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_calculation_executions_request = ListCalculationExecutionsRequest.new(
  session_id: 'SessionId2',
  state_filter: CalculationExecutionState3::CREATING,
  max_results: 100,
  next_token: 'NextToken0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



