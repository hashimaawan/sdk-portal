# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0


# Class Name

`ListApplicationDPUSizesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `application_dpu_sizes` | [`Array[ApplicationDPUSizes]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/application-dpu-sizes.md) | Optional | - |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ruby
list_application_dpu_sizes_output = ListApplicationDPUSizesOutput.new(
  [
    ApplicationDPUSizes.new(
      'ApplicationRuntimeId0',
      [
        113,
        114
      ]
    )
  ],
  'NextToken6'
)
```



