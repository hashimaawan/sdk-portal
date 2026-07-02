# Query Stage Plan

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFu


# Class Name

`QueryStagePlan`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | - |
| `identifier` | `String` | Optional | - |
| `children` | [`Array[QueryStagePlanNode]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-stage-plan-node.md) | Optional | - |
| `remote_sources` | `Array[String]` | Optional | - |


# Example

```ruby
query_stage_plan = QueryStagePlan.new(
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
    ),
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
    ),
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
    'RemoteSources8'
  ]
)
```



