# Update Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlVwZGF0ZVZvbHVtZVJlcXVlc3Q


# Class Name

`UpdateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Required | New Volume name |


# Example

```python
from hetznercloudapi.models.labels_2 import Labels2
from hetznercloudapi.models.update_volume_request import UpdateVolumeRequest

update_volume_request = UpdateVolumeRequest(
    name='database-storage',
    labels=Labels2(
        labelkey='labelkey4'
    )
)
```



