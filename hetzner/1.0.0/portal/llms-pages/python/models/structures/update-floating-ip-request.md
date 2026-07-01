# Update Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZUZsb2F0aW5nSVBSZXF1ZXN0


# Class Name

`UpdateFloatingIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | New Description to set |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New unique name to set |


# Example

```python
import jsonpickle

from hetznercloudapi.models.update_floating_ip_request import UpdateFloatingIPRequest

update_floating_ip_request = UpdateFloatingIPRequest(
    description='Web Frontend',
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='Web Frontend'
)
```



