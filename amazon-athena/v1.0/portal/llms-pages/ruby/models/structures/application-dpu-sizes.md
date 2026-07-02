# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.


# Class Name

`ApplicationDPUSizes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `application_runtime_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `supported_dpu_sizes` | `Array[Integer]` | Optional | - |


# Example

```ruby
application_dpu_sizes = ApplicationDPUSizes.new(
  'ApplicationRuntimeId8',
  [
    137
  ]
)
```



