# Stop Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`StopCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`CalculationExecutionState4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/calculation-execution-state-4.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
stop_calculation_execution_response = StopCalculationExecutionResponse.new(
  state: CalculationExecutionState4::QUEUED,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



