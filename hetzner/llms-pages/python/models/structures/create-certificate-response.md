# Create Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVzcG9uc2U


# Class Name

`CreateCertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/nullable-action.md) | Optional | - |
| `certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/certificate.md) | Required | - |


# Example

```python
from hetznercloudapi.models.certificate import Certificate
from hetznercloudapi.models.create_certificate_response import CreateCertificateResponse
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.issuance_enum import IssuanceEnum
from hetznercloudapi.models.nullable_action import NullableAction
from hetznercloudapi.models.renewal_enum import RenewalEnum
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status_2 import Status2
from hetznercloudapi.models.status_enum import StatusEnum
from hetznercloudapi.models.type_enum import TypeEnum
from hetznercloudapi.models.used_by import UsedBy

create_certificate_response = CreateCertificateResponse(
    certificate=Certificate(
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
    ),
    action=NullableAction(
        command='command6',
        error=Error(
            code='code2',
            message='message4'
        ),
        finished='finished0',
        id=238,
        progress=143.26,
        resources=[
            Resource(
                id=198,
                mtype='type0'
            ),
            Resource(
                id=198,
                mtype='type0'
            ),
            Resource(
                id=198,
                mtype='type0'
            )
        ],
        started='started8',
        status=StatusEnum.RUNNING
    )
)
```



