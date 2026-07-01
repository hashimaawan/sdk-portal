# Volumes Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA


# Class Name

`VolumesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Optional | If true, prevents the Volume from being deleted |


# Example

```python
from hetznercloudapi.models.volumes_actions_change_protection_request import VolumesActionsChangeProtectionRequest

volumes_actions_change_protection_request = VolumesActionsChangeProtectionRequest(
    delete=True
)
```



