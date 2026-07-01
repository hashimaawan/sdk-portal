# Change Loadbalancer Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNoYW5nZUxvYWRiYWxhbmNlckRuc1B0clJlcXVlc3Q


# Class Name

`ChangeLoadbalancerDnsPtrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `str` | Required | Hostname to set as a reverse DNS PTR entry |
| `ip` | `str` | Required | Public IP address for which the reverse DNS entry should be set |


# Example

```python
from hetznercloudapi.models.change_loadbalancer_dns_ptr_request import ChangeLoadbalancerDnsPtrRequest

change_loadbalancer_dns_ptr_request = ChangeLoadbalancerDnsPtrRequest(
    dns_ptr='lb1.example.com',
    ip='1.2.3.4'
)
```



