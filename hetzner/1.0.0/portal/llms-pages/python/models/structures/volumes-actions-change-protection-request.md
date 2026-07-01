# Volumes Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`VolumesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Optional | If true, prevents the Volume from being deleted |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.volumes_actions_change_protection_request import VolumesActionsChangeProtectionRequest

volumes_actions_change_protection_request = VolumesActionsChangeProtectionRequest(
    delete=True,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



