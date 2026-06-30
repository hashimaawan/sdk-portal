# Device Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRkRldmljZU9iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`DeviceObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Optional | The device ID. This ID is unique and persistent to some extent. However, this is not guaranteed and any cached `device_id` should periodically be cleared out and refetched as necessary. |
| `is_active` | `bool` | Optional | If this device is the currently active device. |
| `is_private_session` | `bool` | Optional | If this device is currently in a private session. |
| `is_restricted` | `bool` | Optional | Whether controlling this device is restricted. At present if this is "true" then no Web API commands will be accepted by this device. |
| `name` | `str` | Optional | A human-readable name for the device. Some devices have a name that the user can configure (e.g. \"Loudest speaker\") and some devices have a generic name associated with the manufacturer or device model. |
| `mtype` | `str` | Optional | Device type, such as "computer", "smartphone" or "speaker". |
| `volume_percent` | `int` | Optional | The current volume in percent.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `supports_volume` | `bool` | Optional | If this device can be used to set the volume. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.device_object import DeviceObject

device_object = DeviceObject(
    id='id2',
    is_active=False,
    is_private_session=False,
    is_restricted=False,
    name='Kitchen speaker',
    mtype='computer',
    volume_percent=59,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



