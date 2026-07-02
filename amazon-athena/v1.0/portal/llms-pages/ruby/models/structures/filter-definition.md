# Filter Definition

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkZpbHRlckRlZmluaXRpb24

A string for searching notebook names.

*This model accepts additional fields of type Object.*


# Class Name

`FilterDefinition`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
filter_definition = FilterDefinition.new(
  name: 'Name8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



