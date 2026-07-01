# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `size` | `float` | Required | New Volume size in GB (must be greater than current size) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.volumes_actions_resize_request import VolumesActionsResizeRequest

volumes_actions_resize_request = VolumesActionsResizeRequest(
    size=50,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



