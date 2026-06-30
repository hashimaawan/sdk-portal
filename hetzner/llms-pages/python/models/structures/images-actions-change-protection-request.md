# Images Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Class Name

`ImagesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Optional | If true, prevents the snapshot from being deleted |


# Example

```python
from hetznercloudapi.models.images_actions_change_protection_request import ImagesActionsChangeProtectionRequest

images_actions_change_protection_request = ImagesActionsChangeProtectionRequest(
    delete=True
)
```



