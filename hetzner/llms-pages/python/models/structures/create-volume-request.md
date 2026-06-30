# Create Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNyZWF0ZVZvbHVtZVJlcXVlc3Q


# Class Name

`CreateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `bool` | Optional | Auto-mount Volume after attach. `server` must be provided. |
| `format` | `str` | Optional | Format Volume after creation. One of: `xfs`, `ext4` |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `location` | `str` | Optional | Location to create the Volume in (can be omitted if Server is specified) |
| `name` | `str` | Required | Name of the volume |
| `server` | `int` | Optional | Server to which to attach the Volume once it's created (Volume will be created in the same Location as the server) |
| `size` | `int` | Required | Size of the Volume in GB |


# Example

```python
import jsonpickle

from hetznercloudapi.models.create_volume_request import CreateVolumeRequest

create_volume_request = CreateVolumeRequest(
    name='databases-storage',
    size=42,
    automount=False,
    format='xfs',
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    location='nbg1',
    server=110
)
```



