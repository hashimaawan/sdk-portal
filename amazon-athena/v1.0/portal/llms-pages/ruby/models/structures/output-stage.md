# Output Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRk91dHB1dFN0YWdl


# Class Name

`OutputStage`


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
output_stage = OutputStage.new(
  152,
  'State2',
  86,
  180,
  44,
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



