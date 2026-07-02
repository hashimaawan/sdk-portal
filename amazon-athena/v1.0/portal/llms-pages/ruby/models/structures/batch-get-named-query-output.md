# Batch Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeU91dHB1dA


# Class Name

`BatchGetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_queries` | [`Array[NamedQuery]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/named-query.md) | Optional | - |
| `unprocessed_named_query_ids` | [`Array[UnprocessedNamedQueryId]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/unprocessed-named-query-id.md) | Optional | - |


# Example

```ruby
batch_get_named_query_output = BatchGetNamedQueryOutput.new(
  [
    NamedQuery.new(
      'Name2',
      'Database0',
      'QueryString4',
      'Description4',
      'NamedQueryId0',
      'WorkGroup4'
    ),
    NamedQuery.new(
      'Name2',
      'Database0',
      'QueryString4',
      'Description4',
      'NamedQueryId0',
      'WorkGroup4'
    ),
    NamedQuery.new(
      'Name2',
      'Database0',
      'QueryString4',
      'Description4',
      'NamedQueryId0',
      'WorkGroup4'
    )
  ],
  [
    UnprocessedNamedQueryId.new(
      'NamedQueryId4',
      'ErrorCode6',
      'ErrorMessage4'
    ),
    UnprocessedNamedQueryId.new(
      'NamedQueryId4',
      'ErrorCode6',
      'ErrorMessage4'
    )
  ]
)
```



