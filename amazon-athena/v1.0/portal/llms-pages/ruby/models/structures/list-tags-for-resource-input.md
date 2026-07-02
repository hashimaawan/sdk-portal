# List Tags for Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`ListTagsForResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_arn` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 75` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_tags_for_resource_input = ListTagsForResourceInput.new(
  resource_arn: 'ResourceARN2',
  next_token: 'NextToken8',
  max_results: 140,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



