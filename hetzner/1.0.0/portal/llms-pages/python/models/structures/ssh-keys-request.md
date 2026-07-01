# Ssh Keys Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`SshKeysRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the SSH key |
| `public_key` | `str` | Required | Public key |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.ssh_keys_request import SshKeysRequest

ssh_keys_request = SshKeysRequest(
    name='My ssh key',
    public_key='ssh-rsa AAAjjk76kgf...Xt',
    labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



