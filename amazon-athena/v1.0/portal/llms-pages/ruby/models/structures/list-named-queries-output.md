# List Named Queries Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListNamedQueriesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_ids` | `Array[String]` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_named_queries_output = ListNamedQueriesOutput.new(
  named_query_ids: [
    'NamedQueryIds9'
  ],
  next_token: 'NextToken0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



