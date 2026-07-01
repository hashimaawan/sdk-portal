# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkRuc1B0cg

*This model accepts additional fields of type Any.*


# Class Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `str` | Required | DNS pointer for the specific IP address |
| `ip` | `str` | Required | Single IPv4 or IPv6 address |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.dns_ptr import DnsPtr

dns_ptr = DnsPtr(
    dns_ptr='server.example.com',
    ip='2001:db8::1',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



