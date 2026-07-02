# Batch Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeU91dHB1dA

*This model accepts additional fields of type Object.*


# Class Name

`BatchGetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_queries` | [`Array[NamedQuery]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/named-query.md) | Optional | - |
| `unprocessed_named_query_ids` | [`Array[UnprocessedNamedQueryId]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/unprocessed-named-query-id.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
batch_get_named_query_output = BatchGetNamedQueryOutput.new(
  named_queries: [
    NamedQuery.new(
      name: 'Name2',
      database: 'Database0',
      query_string: 'QueryString4',
      description: 'Description4',
      named_query_id: 'NamedQueryId0',
      work_group: 'WorkGroup4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    NamedQuery.new(
      name: 'Name2',
      database: 'Database0',
      query_string: 'QueryString4',
      description: 'Description4',
      named_query_id: 'NamedQueryId0',
      work_group: 'WorkGroup4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    NamedQuery.new(
      name: 'Name2',
      database: 'Database0',
      query_string: 'QueryString4',
      description: 'Description4',
      named_query_id: 'NamedQueryId0',
      work_group: 'WorkGroup4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  unprocessed_named_query_ids: [
    UnprocessedNamedQueryId.new(
      named_query_id: 'NamedQueryId4',
      error_code: 'ErrorCode6',
      error_message: 'ErrorMessage4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    UnprocessedNamedQueryId.new(
      named_query_id: 'NamedQueryId4',
      error_code: 'ErrorCode6',
      error_message: 'ErrorMessage4',
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



