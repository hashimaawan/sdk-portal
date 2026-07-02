# List Application DPU Sizes Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListApplicationDpuSizesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_application_dpu_sizes_input = ListApplicationDpuSizesInput.new(
  max_results: 76,
  next_token: 'NextToken6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



