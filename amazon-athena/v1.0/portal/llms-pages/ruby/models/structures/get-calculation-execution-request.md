# Get Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`GetCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_calculation_execution_request = GetCalculationExecutionRequest.new(
  calculation_execution_id: 'CalculationExecutionId0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



