# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q


# Class Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `bool` | Optional | Auto-mount the Volume after attaching it |
| `server` | `int` | Required | ID of the Server the Volume will be attached to |


# Example

```python
from hetznercloudapi.models.attach_volume_request import AttachVolumeRequest

attach_volume_request = AttachVolumeRequest(
    server=43,
    automount=False
)
```



