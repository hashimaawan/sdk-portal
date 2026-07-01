# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0


# Class Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `placement_group` | `int` | Required | ID of Placement Group the Server should be added to |


# Example

```python
from hetznercloudapi.models.add_to_placement_group_request import AddToPlacementGroupRequest

add_to_placement_group_request = AddToPlacementGroupRequest(
    placement_group=1
)
```



