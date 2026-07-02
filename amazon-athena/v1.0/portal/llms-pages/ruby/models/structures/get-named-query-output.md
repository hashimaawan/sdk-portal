# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query` | [`NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/named-query-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_named_query_output = GetNamedQueryOutput.new(
  named_query: NamedQuery1.new(
    name: 'Name0',
    database: 'Database8',
    query_string: 'QueryString2',
    description: 'Description6',
    named_query_id: 'NamedQueryId2',
    work_group: 'WorkGroup2',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



