# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ

*This model accepts additional fields of type Any.*


# Class Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | `str` | Optional | - |
| `network` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.private_net import PrivateNet

private_net = PrivateNet(
    ip='10.0.0.2',
    network=4711,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



