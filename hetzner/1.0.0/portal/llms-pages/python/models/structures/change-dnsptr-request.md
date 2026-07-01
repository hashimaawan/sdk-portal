# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q


# Class Name

`ChangeDNSPTRRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `str` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` |
| `ip` | `str` | Required | IP address for which to set the reverse DNS entry |


# Example

```python
from hetznercloudapi.models.change_dnsptr_request import ChangeDNSPTRRequest

change_dnsptr_request = ChangeDNSPTRRequest(
    dns_ptr='server02.example.com',
    ip='1.2.3.4'
)
```



