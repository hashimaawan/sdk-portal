# List Tags for Resource Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListTagsForResourceOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tags` | [`Array[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/tag.md) | Optional | - |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_tags_for_resource_output = ListTagsForResourceOutput.new(
  tags: [
    Tag.new(
      key: 'Key0',
      value: 'Value6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  next_token: 'NextToken4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



