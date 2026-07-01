# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `bool` | Optional | Auto-mount the Volume after attaching it |
| `server` | `int` | Required | ID of the Server the Volume will be attached to |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.attach_volume_request import AttachVolumeRequest

attach_volume_request = AttachVolumeRequest(
    server=43,
    automount=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



