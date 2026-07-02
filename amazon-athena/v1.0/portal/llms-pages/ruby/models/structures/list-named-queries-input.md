# List Named Queries Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`ListNamedQueriesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 50` |
| `work_group` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_named_queries_input = ListNamedQueriesInput.new(
  next_token: 'NextToken0',
  max_results: 50,
  work_group: 'WorkGroup2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



