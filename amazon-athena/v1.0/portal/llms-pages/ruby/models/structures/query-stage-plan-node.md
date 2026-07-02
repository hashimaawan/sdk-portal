# Query Stage Plan Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFuTm9kZQ

Stage plan information such as name, identifier, sub plans, and remote sources.


# Class Name

`QueryStagePlanNode`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | - |
| `identifier` | `String` | Optional | - |
| `children` | [`Array[QueryStagePlanNode]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-stage-plan-node.md) | Optional | - |
| `remote_sources` | `Array[String]` | Optional | - |


# Example

```ruby
query_stage_plan_node = QueryStagePlanNode.new(
  'Name0',
  'Identifier6',
  [
    QueryStagePlanNode.new(
      'Name6',
      'Identifier2',
      [
        QueryStagePlanNode.new(
          nil,
          nil,
          [],
          []
        )
      ],
      [
        'RemoteSources4',
        'RemoteSources5',
        'RemoteSources6'
      ]
    )
  ],
  [
    'RemoteSources8',
    'RemoteSources9',
    'RemoteSources0'
  ]
)
```



