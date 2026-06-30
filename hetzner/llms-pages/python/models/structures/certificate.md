# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate` | `str` | Required | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding |
| `created` | `str` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `domain_names` | `List[str]` | Required | Domains and subdomains covered by the Certificate |
| `fingerprint` | `str` | Required | SHA256 fingerprint of the Certificate |
| `id` | `int` | Required | ID of the Resource |
| `labels` | `Dict[str, str]` | Required | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the Resource. Must be unique per Project. |
| `not_valid_after` | `str` | Required | Point in time when the Certificate stops being valid (in ISO-8601 format) |
| `not_valid_before` | `str` | Required | Point in time when the Certificate becomes valid (in ISO-8601 format) |
| `status` | [`Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/status-2.md) | Optional | Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates |
| `mtype` | [`TypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type.md) | Optional | Type of the Certificate |
| `used_by` | [`List[UsedBy]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/used-by.md) | Required | Resources currently using the Certificate |


# Example

```python
from hetznercloudapi.models.certificate import Certificate
from hetznercloudapi.models.issuance_enum import IssuanceEnum
from hetznercloudapi.models.renewal_enum import RenewalEnum
from hetznercloudapi.models.status_2 import Status2
from hetznercloudapi.models.type_enum import TypeEnum
from hetznercloudapi.models.used_by import UsedBy

certificate = Certificate(
    certificate='-----BEGIN CERTIFICATE-----\n...',
    created='2016-01-30T23:55:00+00:00',
    domain_names=[
        'example.com',
        'webmail.example.com',
        'www.example.com'
    ],
    fingerprint='03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f',
    id=42,
    labels={
        'key0': 'labels8',
        'key1': 'labels7',
        'key2': 'labels6'
    },
    name='my-resource',
    not_valid_after='2019-07-08T09:59:59+00:00',
    not_valid_before='2019-01-08T10:00:00+00:00',
    used_by=[
        UsedBy(
            id=4711,
            mtype='load_balancer'
        )
    ],
    status=Status2(
        error=None,
        issuance=IssuanceEnum.COMPLETED,
        renewal=RenewalEnum.FAILED
    ),
    mtype=TypeEnum.UPLOADED
)
```



