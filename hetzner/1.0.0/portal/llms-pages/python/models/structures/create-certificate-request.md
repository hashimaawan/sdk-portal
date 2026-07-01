# Create Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVxdWVzdA


# Class Name

`CreateCertificateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate` | `str` | Optional | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding. Required for type `uploaded` Certificates. |
| `domain_names` | `List[str]` | Optional | Domains and subdomains that should be contained in the Certificate issued by *Let's Encrypt*. Required for type `managed` Certificates. |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the Certificate |
| `private_key` | `str` | Optional | Certificate key in PEM format. Required for type `uploaded` Certificates. |
| `mtype` | [`Type1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-1.md) | Optional | Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`. |


# Example

```python
import jsonpickle

from hetznercloudapi.models.create_certificate_request import CreateCertificateRequest
from hetznercloudapi.models.type_1_enum import Type1Enum

create_certificate_request = CreateCertificateRequest(
    name='my website cert',
    certificate='-----BEGIN CERTIFICATE-----\n...',
    domain_names=[
        'domain_names2'
    ],
    labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    private_key='-----BEGIN PRIVATE KEY-----\n...',
    mtype=Type1Enum.UPLOADED
)
```



