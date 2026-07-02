# Query Stage Plan Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFuTm9kZQ

Stage plan information such as name, identifier, sub plans, and remote sources.


# Class Name

`QueryStagePlanNode`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | - |
| `identifier` | `str` | Optional | - |
| `children` | [`List[QueryStagePlanNode]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-stage-plan-node.md) | Optional | - |
| `remote_sources` | `List[str]` | Optional | - |


# Example

```python
from amazonathena.models.query_stage_plan_node import QueryStagePlanNode

query_stage_plan_node = QueryStagePlanNode(
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
        )
    ],
    remote_sources=[
        'RemoteSources8',
        'RemoteSources9',
        'RemoteSources0'
    ]
)
```



