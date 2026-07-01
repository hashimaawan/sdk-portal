# Ssh Keys Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Any.*


# Class Name

`SshKeysResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/meta.md) | Optional | - |
| `ssh_keys` | [`List[SshKey]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/ssh-key.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.ssh_key import SshKey
from hetznercloudapi.models.ssh_keys_response import SshKeysResponse

ssh_keys_response = SshKeysResponse(
    ssh_keys=[
        SshKey(
            created='2016-01-30T23:55:00+00:00',
            fingerprint='b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
            id=42,
            labels={
                'key0': 'labels4',
                'key1': 'labels5',
                'key2': 'labels6'
            },
            name='my-resource',
            public_key='ssh-rsa AAAjjk76kgf...Xt',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



