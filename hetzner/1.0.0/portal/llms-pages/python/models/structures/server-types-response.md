# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl


# Class Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server_types` | [`List[ServerTypes7]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-types-7.md) | Required | - |


# Example

```python
from hetznercloudapi.models.cpu_type_enum import CpuTypeEnum
from hetznercloudapi.models.price_9 import Price9
from hetznercloudapi.models.price_hourly_8 import PriceHourly8
from hetznercloudapi.models.price_monthly_10 import PriceMonthly10
from hetznercloudapi.models.server_types_7 import ServerTypes7
from hetznercloudapi.models.server_types_response import ServerTypesResponse
from hetznercloudapi.models.storage_type_enum import StorageTypeEnum

server_types_response = ServerTypesResponse(
    server_types=[
        ServerTypes7(
            cores=1,
            cpu_type=CpuTypeEnum.SHARED,
            deprecated=False,
            description='CX11',
            disk=24,
            id=1,
            memory=1,
            name='cx11',
            prices=[
                Price9(
                    location='fsn1',
                    price_hourly=PriceHourly8(
                        gross='1.1900000000000000',
                        net='1.0000000000'
                    ),
                    price_monthly=PriceMonthly10(
                        gross='1.1900000000000000',
                        net='1.0000000000'
                    )
                )
            ],
            storage_type=StorageTypeEnum.LOCAL
        )
    ]
)
```



