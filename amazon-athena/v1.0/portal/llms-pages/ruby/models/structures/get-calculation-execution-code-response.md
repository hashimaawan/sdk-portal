# Get Calculation Execution Code Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`GetCalculationExecutionCodeResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code_block` | `String` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_calculation_execution_code_response = GetCalculationExecutionCodeResponse.new(
  code_block: 'CodeBlock2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



