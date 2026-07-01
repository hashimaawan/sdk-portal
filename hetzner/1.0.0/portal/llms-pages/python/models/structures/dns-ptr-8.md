# Dns Ptr 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkRuc1B0cjg

*This model accepts additional fields of type Any.*


# Class Name

`DnsPtr8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `str` | Required | DNS pointer for the specific IP address |
| `ip` | `str` | Required | Single IPv6 address of this Server for which the reverse DNS entry has been set up |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.dns_ptr_8 import DnsPtr8

dns_ptr_8 = DnsPtr8(
    dns_ptr='server.example.com',
    ip='2001:db8::1',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



