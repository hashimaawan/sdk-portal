# Ipv 44

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRklwdjQ0

IP address (v4) and its reverse DNS entry of this Server

*This model accepts additional fields of type Any.*


# Class Name

`Ipv44`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `bool` | Required | If the IP is blocked by our anti abuse dept |
| `dns_ptr` | `str` | Required | Reverse DNS PTR entry for the IPv4 addresses of this Server |
| `id` | `int` | Optional | ID of the Resource |
| `ip` | `str` | Required | IP address (v4) of this Server |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.ipv_44 import Ipv44

ipv_44 = Ipv44(
    blocked=False,
    dns_ptr='server01.example.com',
    ip='1.2.3.4',
    id=42,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



