# Images Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`ImagesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Optional | If true, prevents the snapshot from being deleted |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.images_actions_change_protection_request import ImagesActionsChangeProtectionRequest

images_actions_change_protection_request = ImagesActionsChangeProtectionRequest(
    delete=True,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



