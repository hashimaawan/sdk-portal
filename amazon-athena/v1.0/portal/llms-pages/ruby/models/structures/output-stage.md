# Output Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRk91dHB1dFN0YWdl

*This model accepts additional fields of type Object.*


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
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
output_stage = OutputStage.new(
  stage_id: 152,
  state: 'State2',
  output_bytes: 86,
  output_rows: 180,
  input_bytes: 44,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



