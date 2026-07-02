# Result Reuse Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbjE

*This model accepts additional fields of type Object.*


# Class Name

`ResultReuseConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `result_reuse_by_age_configuration` | [`ResultReuseByAgeConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
result_reuse_configuration1 = ResultReuseConfiguration1.new(
  result_reuse_by_age_configuration: ResultReuseByAgeConfiguration2.new(
    enabled: false,
    max_age_in_minutes: 26,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



