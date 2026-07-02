# Query Stage Plan Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFuTm9kZQ

Stage plan information such as name, identifier, sub plans, and remote sources.

*This model accepts additional fields of type Object.*


# Class Name

`QueryStagePlanNode`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | - |
| `identifier` | `String` | Optional | - |
| `children` | [`Array[QueryStagePlanNode]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-stage-plan-node.md) | Optional | - |
| `remote_sources` | `Array[String]` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
query_stage_plan_node = QueryStagePlanNode.new(
  name: 'Name0',
  identifier: 'Identifier6',
  children: [
    QueryStagePlanNode.new(
      name: 'Name6',
      identifier: 'Identifier2',
      children: [
        QueryStagePlanNode.new
      ],
      remote_sources: [
        'RemoteSources4',
        'RemoteSources5',
        'RemoteSources6'
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  remote_sources: [
    'RemoteSources8',
    'RemoteSources9',
    'RemoteSources0'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



