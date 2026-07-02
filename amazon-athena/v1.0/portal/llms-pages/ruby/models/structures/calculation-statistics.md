# Calculation Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdGlzdGljcw

Contains statistics for a notebook calculation.

*This model accepts additional fields of type Object.*


# Class Name

`CalculationStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dpu_execution_in_millis` | `Integer` | Optional | - |
| `progress` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
calculation_statistics = CalculationStatistics.new(
  dpu_execution_in_millis: 242,
  progress: 'Progress6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



