# Stop Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlcXVlc3Q


# Class Name

`StopCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |


# Example

```ruby
stop_calculation_execution_request = StopCalculationExecutionRequest.new(
  'CalculationExecutionId2'
)
```



