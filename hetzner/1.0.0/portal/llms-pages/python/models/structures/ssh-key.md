# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNzaEtleQ


# Class Name

`SshKey`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `str` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `fingerprint` | `str` | Required | Fingerprint of public key |
| `id` | `int` | Required | ID of the Resource |
| `labels` | `Dict[str, str]` | Required | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the Resource. Must be unique per Project. |
| `public_key` | `str` | Required | Public key |


# Example

```python
from hetznercloudapi.models.ssh_key import SshKey

ssh_key = SshKey(
    created='2016-01-30T23:55:00+00:00',
    fingerprint='b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
    id=42,
    labels={
        'key0': 'labels0'
    },
    name='my-resource',
    public_key='ssh-rsa AAAjjk76kgf...Xt'
)
```



