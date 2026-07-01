# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA


# Class Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `size` | `float` | Required | New Volume size in GB (must be greater than current size) |


# Example

```python
from hetznercloudapi.models.volumes_actions_resize_request import VolumesActionsResizeRequest

volumes_actions_resize_request = VolumesActionsResizeRequest(
    size=50
)
```



