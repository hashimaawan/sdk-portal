# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`ChangeDnsptrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `str` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` |
| `ip` | `str` | Required | IP address for which to set the reverse DNS entry |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.change_dnsptr_request import ChangeDnsptrRequest

change_dnsptr_request = ChangeDnsptrRequest(
    dns_ptr='server02.example.com',
    ip='1.2.3.4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



