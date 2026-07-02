# Query Stage Plan

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFu


# Class Name

`QueryStagePlan`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | - |
| `identifier` | `str` | Optional | - |
| `children` | [`List[QueryStagePlanNode]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-stage-plan-node.md) | Optional | - |
| `remote_sources` | `List[str]` | Optional | - |


# Example

```python
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
            ]
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
            ]
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
            ]
        )
    ],
    remote_sources=[
        'RemoteSources8'
    ]
)
```



