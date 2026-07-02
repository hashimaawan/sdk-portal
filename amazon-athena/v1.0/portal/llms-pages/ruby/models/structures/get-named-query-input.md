# Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`GetNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_named_query_input = GetNamedQueryInput.new(
  named_query_id: 'NamedQueryId8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



