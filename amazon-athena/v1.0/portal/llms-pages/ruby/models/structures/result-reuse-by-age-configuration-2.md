# Result Reuse by Age Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9uMg

*This model accepts additional fields of type Object.*


# Class Name

`ResultReuseByAgeConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `TrueClass \| FalseClass` | Required | - |
| `max_age_in_minutes` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 10080` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
result_reuse_by_age_configuration2 = ResultReuseByAgeConfiguration2.new(
  enabled: false,
  max_age_in_minutes: 254,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



