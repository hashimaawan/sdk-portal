# Session Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0aXN0aWNz

Contains statistics for a session.

*This model accepts additional fields of type Object.*


# Class Name

`SessionStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dpu_execution_in_millis` | `Integer` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
session_statistics = SessionStatistics.new(
  dpu_execution_in_millis: 136,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



