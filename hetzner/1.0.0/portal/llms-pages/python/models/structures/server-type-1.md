# Server Type 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlclR5cGUx

Type of Server - determines how much ram, disk and cpu a Server has


# Class Name

`ServerType1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cores` | `float` | Required | Number of cpu cores a Server of this type will have |
| `cpu_type` | [`CpuTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/cpu-type.md) | Required | Type of cpu |
| `deprecated` | `bool` | Required | True if Server type is deprecated |
| `description` | `str` | Required | Description of the Server type |
| `disk` | `float` | Required | Disk size a Server of this type will have in GB |
| `id` | `int` | Required | ID of the Server type |
| `memory` | `float` | Required | Memory a Server of this type will have in GB |
| `name` | `str` | Required | Unique identifier of the Server type |
| `prices` | [`List[Price9]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-9.md) | Required | Prices in different Locations |
| `storage_type` | [`StorageTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. |


# Example

```python
from hetznercloudapi.models.cpu_type_enum import CpuTypeEnum
from hetznercloudapi.models.price_9 import Price9
from hetznercloudapi.models.price_hourly_8 import PriceHourly8
from hetznercloudapi.models.price_monthly_10 import PriceMonthly10
from hetznercloudapi.models.server_type_1 import ServerType1
from hetznercloudapi.models.storage_type_enum import StorageTypeEnum

server_type_1 = ServerType1(
    cores=1,
    cpu_type=CpuTypeEnum.SHARED,
    deprecated=False,
    description='CX11',
    disk=25,
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
```



