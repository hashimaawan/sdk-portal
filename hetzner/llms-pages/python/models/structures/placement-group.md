# Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vw


# Class Name

`PlacementGroup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `str` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `int` | Required | ID of the Resource |
| `labels` | `Dict[str, str]` | Required | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the Resource. Must be unique per Project. |
| `servers` | `List[int]` | Required | Array of IDs of Servers that are part of this Placement Group |
| `mtype` | `str` | Required, Constant | Type of the Placement Group<br><br>**Value**: `"spread"` |


# Example

```python
from hetznercloudapi.models.placement_group import PlacementGroup

placement_group = PlacementGroup(
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
```



