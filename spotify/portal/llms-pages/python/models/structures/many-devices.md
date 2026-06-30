# Many Devices

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRk1hbnlEZXZpY2Vz

*This model accepts additional fields of type Any.*


# Class Name

`ManyDevices`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `devices` | [`List[DeviceObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/device-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.device_object import DeviceObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.many_devices import ManyDevices

many_devices = ManyDevices(
    devices=[
        DeviceObject(
            id='id4',
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
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



