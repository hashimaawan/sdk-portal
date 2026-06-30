# Server Types 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzMg


# Class Name

`ServerTypes2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `float` | Required | ID of the Server type the price is for |
| `name` | `str` | Required | Name of the Server type the price is for |
| `prices` | [`List[Price9]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/price-9.md) | Required | Server type costs per Location |


# Example

```python
from hetznercloudapi.models.price_9 import Price9
from hetznercloudapi.models.price_hourly_8 import PriceHourly8
from hetznercloudapi.models.price_monthly_10 import PriceMonthly10
from hetznercloudapi.models.server_types_2 import ServerTypes2

server_types_2 = ServerTypes2(
    id=4,
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
    ]
)
```



