# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resource_arn` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tag_keys` | `Array[String]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
untag_resource_input = UntagResourceInput.new(
  resource_arn: 'ResourceARN4',
  tag_keys: [
    'TagKeys9'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



