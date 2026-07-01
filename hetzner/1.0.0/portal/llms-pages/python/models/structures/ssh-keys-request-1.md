# Ssh Keys Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdDE

*This model accepts additional fields of type Any.*


# Class Name

`SshKeysRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New name Name to set |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.ssh_keys_request_1 import SshKeysRequest1

ssh_keys_request_1 = SshKeysRequest1(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='My ssh key',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



