# List Application DPU Sizes Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzSW5wdXQ


# Class Name

`ListApplicationDPUSizesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ruby
list_application_dpu_sizes_input = ListApplicationDPUSizesInput.new(
  76,
  'NextToken6'
)
```



