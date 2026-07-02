# Query Stage Plan

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFu

*This model accepts additional fields of type Any.*


# Class Name

`QueryStagePlan`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | - |
| `identifier` | `str` | Optional | - |
| `children` | [`List[QueryStagePlanNode]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-stage-plan-node.md) | Optional | - |
| `remote_sources` | `List[str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.query_stage_plan import QueryStagePlan
from amazonathena.models.query_stage_plan_node import QueryStagePlanNode

query_stage_plan = QueryStagePlan(
    name='Name0',
    identifier='Identifier6',
    children=[
        QueryStagePlanNode(
            name='Name6',
            identifier='Identifier2',
            children=[
                QueryStagePlanNode()
            ],
            remote_sources=[
                'RemoteSources4',
                'RemoteSources5',
                'RemoteSources6'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        QueryStagePlanNode(
            name='Name6',
            identifier='Identifier2',
            children=[
                QueryStagePlanNode()
            ],
            remote_sources=[
                'RemoteSources4',
                'RemoteSources5',
                'RemoteSources6'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        QueryStagePlanNode(
            name='Name6',
            identifier='Identifier2',
            children=[
                QueryStagePlanNode()
            ],
            remote_sources=[
                'RemoteSources4',
                'RemoteSources5',
                'RemoteSources6'
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    remote_sources=[
        'RemoteSources8'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



