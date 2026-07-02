# Tag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlRhZ1Jlc291cmNlSW5wdXQ


# Class Name

`TagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_arn` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tags` | [`Array[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/tag.md) | Required | - |


# Example

```ruby
tag_resource_input = TagResourceInput.new(
  'ResourceARN0',
  [
    Tag.new(
      'Key0',
      'Value6'
    )
  ]
)
```



