# Query Stage Plan

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFu

*This model accepts additional fields of type Object.*


# Class Name

`QueryStagePlan`


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
query_stage_plan = QueryStagePlan.new(
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
    ),
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
    ),
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
    'RemoteSources8'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



