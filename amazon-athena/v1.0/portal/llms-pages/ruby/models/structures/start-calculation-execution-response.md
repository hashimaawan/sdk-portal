# Start Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`StartCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `state` | [`CalculationExecutionState4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/calculation-execution-state-4.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
start_calculation_execution_response = StartCalculationExecutionResponse.new(
  calculation_execution_id: 'CalculationExecutionId0',
  state: CalculationExecutionState4::CANCELING,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



