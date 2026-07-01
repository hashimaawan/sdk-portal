# Price 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNlOA


# Class Name

`Price8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `str` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-hourly-7.md) | Required | Hourly costs for a Primary IP type in this Location |
| `price_monthly` | [`PriceMonthly9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-monthly-9.md) | Required | Monthly costs for a Primary IP type in this Location |


# Example

```python
from hetznercloudapi.models.price_8 import Price8
from hetznercloudapi.models.price_hourly_7 import PriceHourly7
from hetznercloudapi.models.price_monthly_9 import PriceMonthly9

price_8 = Price8(
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
```



