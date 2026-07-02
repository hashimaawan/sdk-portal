# Query Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2U

Stage statistics such as input and output rows and bytes, execution time and stage state. This information also includes substages and the query stage plan.

*This model accepts additional fields of type Object.*


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
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
query_stage = QueryStage.new(
  stage_id: 162,
  state: 'State0',
  output_bytes: 76,
  output_rows: 190,
  input_bytes: 222,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



