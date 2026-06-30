# Ssh Keys Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdDE


# Class Name

`SshKeysRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New name Name to set |


# Example

```python
import jsonpickle

from hetznercloudapi.models.ssh_keys_request_1 import SshKeysRequest1

ssh_keys_request_1 = SshKeysRequest1(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='My ssh key'
)
```



