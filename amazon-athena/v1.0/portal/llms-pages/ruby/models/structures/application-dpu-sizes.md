# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.

*This model accepts additional fields of type Object.*


# Class Name

`ApplicationDpuSizes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `application_runtime_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `supported_dpu_sizes` | `Array[Integer]` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
application_dpu_sizes = ApplicationDpuSizes.new(
  application_runtime_id: 'ApplicationRuntimeId8',
  supported_dpu_sizes: [
    137
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



