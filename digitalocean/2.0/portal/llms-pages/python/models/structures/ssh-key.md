# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlNzaEtleQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`SshKey`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fingerprint` | `str` | Optional, Read-only | A unique identifier that differentiates this key from other keys using  a format that SSH recognizes. The fingerprint is created when the key is added to your account. |
| `id` | `int` | Optional, Read-only | A unique identification number for this key. Can be used to embed a  specific SSH key into a Droplet. |
| `name` | `str` | Required | A human-readable display name for this key, used to easily identify the SSH keys when they are displayed. |
| `public_key` | `str` | Required | The entire public key string that was uploaded. Embedded into the root user's `authorized_keys` file if you include this key during Droplet creation. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.ssh_key import SshKey

ssh_key = SshKey(
    name='My SSH Public Key',
    public_key='ssh-rsa AEXAMPLEaC1yc2EAAAADAQABAAAAQQDDHr/jh2Jy4yALcK4JyWbVkPRaWmhck3IgCoeOO3z1e2dBowLh64QAM+Qb72pxekALga2oi4GvT+TlWNhzPH4V example',
    fingerprint='3b:16:bf:e4:8b:00:8b:b8:59:8c:a9:d3:f0:19:45:fa',
    id=512189,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



