# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q


# Class Name

`UpdatePrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_delete` | `bool` | Optional | Delete this Primary IP when the resource it is assigned to is deleted |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New unique name to set |


# Example

```python
import jsonpickle

from hetznercloudapi.models.update_primary_ip_request import UpdatePrimaryIPRequest

update_primary_ip_request = UpdatePrimaryIPRequest(
    auto_delete=True,
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='my-ip'
)
```



