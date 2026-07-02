# Result Reuse by Age Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9u

Specifies whether previous query results are reused, and if so, their maximum age.

*This model accepts additional fields of type Object.*


# Class Name

`ResultReuseByAgeConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `TrueClass \| FalseClass` | Required | - |
| `max_age_in_minutes` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 10080` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
result_reuse_by_age_configuration = ResultReuseByAgeConfiguration.new(
  enabled: false,
  max_age_in_minutes: 32,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



