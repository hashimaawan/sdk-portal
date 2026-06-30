# Create Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVzcG9uc2U


# Class Name

`CreatePlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/nullable-action.md) | Optional | - |
| `placement_group` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/placement-group.md) | Required | - |


# Example

```python
from hetznercloudapi.models.create_placement_group_response import CreatePlacementGroupResponse
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.nullable_action import NullableAction
from hetznercloudapi.models.placement_group import PlacementGroup
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status_enum import StatusEnum

create_placement_group_response = CreatePlacementGroupResponse(
    placement_group=PlacementGroup(
        created='2016-01-30T23:55:00+00:00',
        id=42,
        labels={
            'key0': 'labels4'
        },
        name='my-resource',
        servers=[
            42
        ]
    ),
    action=NullableAction(
        command='command6',
        error=Error(
            code='code2',
            message='message4'
        ),
        finished='finished0',
        id=238,
        progress=143.26,
        resources=[
            Resource(
                id=198,
                mtype='type0'
            ),
            Resource(
                id=198,
                mtype='type0'
            ),
            Resource(
                id=198,
                mtype='type0'
            )
        ],
        started='started8',
        status=StatusEnum.RUNNING
    )
)
```



