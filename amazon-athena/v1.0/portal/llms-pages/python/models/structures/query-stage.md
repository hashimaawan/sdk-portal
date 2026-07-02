# Query Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2U

Stage statistics such as input and output rows and bytes, execution time and stage state. This information also includes substages and the query stage plan.

*This model accepts additional fields of type Any.*


# Class Name

`QueryStage`


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

from amazonathena.models.query_stage import QueryStage

query_stage = QueryStage(
    stage_id=162,
    state='State0',
    output_bytes=76,
    output_rows=190,
    input_bytes=222,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



