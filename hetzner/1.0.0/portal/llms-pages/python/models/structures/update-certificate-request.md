# Update Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZUNlcnRpZmljYXRlUmVxdWVzdA


# Class Name

`UpdateCertificateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New Certificate name |


# Example

```python
import jsonpickle

from hetznercloudapi.models.update_certificate_request import UpdateCertificateRequest

update_certificate_request = UpdateCertificateRequest(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='my website cert'
)
```



