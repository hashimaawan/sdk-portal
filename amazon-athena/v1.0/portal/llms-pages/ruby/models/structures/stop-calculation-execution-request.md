# Stop Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`StopCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
stop_calculation_execution_request = StopCalculationExecutionRequest.new(
  calculation_execution_id: 'CalculationExecutionId2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



