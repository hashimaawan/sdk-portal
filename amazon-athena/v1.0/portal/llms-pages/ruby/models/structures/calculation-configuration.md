# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.

*This model accepts additional fields of type Object.*


# Class Name

`CalculationConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code_block` | `String` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
calculation_configuration = CalculationConfiguration.new(
  code_block: 'CodeBlock6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



