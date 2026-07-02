# Result Reuse Information 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24y

*This model accepts additional fields of type Object.*


# Class Name

`ResultReuseInformation2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reused_previous_result` | `TrueClass \| FalseClass` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
result_reuse_information2 = ResultReuseInformation2.new(
  reused_previous_result: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



