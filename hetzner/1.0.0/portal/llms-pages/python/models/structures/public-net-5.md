# Public Net 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlB1YmxpY05ldDU

Public Network options

*This model accepts additional fields of type Any.*


# Class Name

`PublicNet5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enable_ipv_4` | `bool` | Optional | Attach an IPv4 on the public NIC. If false, no IPv4 address will be attached. Defaults to true. |
| `enable_ipv_6` | `bool` | Optional | Attach an IPv6 on the public NIC. If false, no IPv6 address will be attached. Defaults to true. |
| `ipv_4` | `int` | Optional | ID of the ipv4 Primary IP to use. If omitted and enable_ipv4 is true, a new ipv4 Primary IP will automatically be created. |
| `ipv_6` | `int` | Optional | ID of the ipv6 Primary IP to use. If omitted and enable_ipv6 is true, a new ipv6 Primary IP will automatically be created. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.public_net_5 import PublicNet5

public_net_5 = PublicNet5(
    enable_ipv_4=False,
    enable_ipv_6=False,
    ipv_4=204,
    ipv_6=196,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



