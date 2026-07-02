# Result Reuse Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbg

Specifies the query result reuse behavior for the query.

*This model accepts additional fields of type Object.*


# Class Name

`ResultReuseConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `result_reuse_by_age_configuration` | [`ResultReuseByAgeConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
result_reuse_configuration = ResultReuseConfiguration.new(
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



