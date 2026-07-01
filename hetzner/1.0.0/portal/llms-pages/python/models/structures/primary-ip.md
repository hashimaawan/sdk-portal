# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaW1hcnlJcA


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prices` | [`List[Price8]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-8.md) | Required | Primary IP type costs per Location |
| `mtype` | [`Type49Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-49.md) | Required | The type of the Primary IP |


# Example

```python
from hetznercloudapi.models.price_8 import Price8
from hetznercloudapi.models.price_hourly_7 import PriceHourly7
from hetznercloudapi.models.price_monthly_9 import PriceMonthly9
from hetznercloudapi.models.primary_ip import PrimaryIp
from hetznercloudapi.models.type_49_enum import Type49Enum

primary_ip = PrimaryIp(
    prices=[
        Price8(
            location='fsn1',
            price_hourly=PriceHourly7(
                gross='1.1900000000000000',
                net='1.0000000000'
            ),
            price_monthly=PriceMonthly9(
                gross='1.1900000000000000',
                net='1.0000000000'
            )
        )
    ],
    mtype=Type49Enum.IPV4
)
```



