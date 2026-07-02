# Output Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRk91dHB1dFN0YWdl

*This model accepts additional fields of type Any.*


# Class Name

`OutputStage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `stage_id` | `int` | Optional | - |
| `state` | `str` | Optional | - |
| `output_bytes` | `int` | Optional | - |
| `output_rows` | `int` | Optional | - |
| `input_bytes` | `int` | Optional | - |
| `input_rows` | `int` | Optional | - |
| `execution_time` | `int` | Optional | - |
| `query_stage_plan` | [`QueryStagePlan`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-stage-plan.md) | Optional | - |
| `sub_stages` | [`List[QueryStage]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-stage.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.output_stage import OutputStage

output_stage = OutputStage(
    stage_id=152,
    state='State2',
    output_bytes=86,
    output_rows=180,
    input_bytes=44,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



