# Update Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlVwZGF0ZUZpcmV3YWxsUmVxdWVzdA


# Class Name

`UpdateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New Firewall name |


# Example

```python
import jsonpickle

from hetznercloudapi.models.update_firewall_request import UpdateFirewallRequest

update_firewall_request = UpdateFirewallRequest(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='new-name'
)
```



