# Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwUmVzcG9uc2U


# Class Name

`PlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `placement_group` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/placement-group.md) | Required | - |


# Example

```python
from hetznercloudapi.models.placement_group import PlacementGroup
from hetznercloudapi.models.placement_group_response import PlacementGroupResponse

placement_group_response = PlacementGroupResponse(
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
    )
)
```



