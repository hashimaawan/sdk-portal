# Result Reuse Information

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24

Contains information about whether the result of a previous query was reused.

*This model accepts additional fields of type Object.*


# Class Name

`ResultReuseInformation`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reused_previous_result` | `TrueClass \| FalseClass` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
result_reuse_information = ResultReuseInformation.new(
  reused_previous_result: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



