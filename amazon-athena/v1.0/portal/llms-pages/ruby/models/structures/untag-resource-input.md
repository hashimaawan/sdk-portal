# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_arn` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tag_keys` | `Array[String]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```ruby
untag_resource_input = UntagResourceInput.new(
  'ResourceARN4',
  [
    'TagKeys9'
  ]
)
```



