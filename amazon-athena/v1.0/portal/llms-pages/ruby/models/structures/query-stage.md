# Query Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2U

Stage statistics such as input and output rows and bytes, execution time and stage state. This information also includes substages and the query stage plan.


# Class Name

`QueryStage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `stage_id` | `Integer` | Optional | - |
| `state` | `String` | Optional | - |
| `output_bytes` | `Integer` | Optional | - |
| `output_rows` | `Integer` | Optional | - |
| `input_bytes` | `Integer` | Optional | - |
| `input_rows` | `Integer` | Optional | - |
| `execution_time` | `Integer` | Optional | - |
| `query_stage_plan` | [`QueryStagePlan`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-stage-plan.md) | Optional | - |
| `sub_stages` | [`Array[QueryStage]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/query-stage.md) | Optional | - |


# Example

```ruby
query_stage = QueryStage.new(
  162,
  'State0',
  76,
  190,
  222,
  nil,
  nil,
  QueryStagePlan.new(
    nil,
    nil,
    [],
    []
  ),
  []
)
```



