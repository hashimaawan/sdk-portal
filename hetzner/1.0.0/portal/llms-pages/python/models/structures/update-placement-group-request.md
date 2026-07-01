# Update Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA


# Class Name

`UpdatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New PlacementGroup name |


# Example

```python
import jsonpickle

from hetznercloudapi.models.update_placement_group_request import UpdatePlacementGroupRequest

update_placement_group_request = UpdatePlacementGroupRequest(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='my Placement Group'
)
```



