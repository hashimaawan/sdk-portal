# Tag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlRhZ1Jlc291cmNlSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`TagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_arn` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tags` | [`Array[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/tag.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
tag_resource_input = TagResourceInput.new(
  resource_arn: 'ResourceARN0',
  tags: [
    Tag.new(
      key: 'Key0',
      value: 'Value6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



