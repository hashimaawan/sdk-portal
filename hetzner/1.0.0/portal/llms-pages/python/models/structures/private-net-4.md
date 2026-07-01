# Private Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ0

*This model accepts additional fields of type Any.*


# Class Name

`PrivateNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alias_ips` | `List[str]` | Optional | - |
| `ip` | `str` | Optional | - |
| `mac_address` | `str` | Optional | - |
| `network` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.private_net_4 import PrivateNet4

private_net_4 = PrivateNet4(
    alias_ips=[
        'alias_ips0'
    ],
    ip='10.0.0.2',
    mac_address='86:00:ff:2a:7d:e1',
    network=4711,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



