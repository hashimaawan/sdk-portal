# Price 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlByaWNlOQ


# Class Name

`Price9`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `str` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/price-hourly-8.md) | Required | Hourly costs for a Server type in this Location |
| `price_monthly` | [`PriceMonthly10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/price-monthly-10.md) | Required | Monthly costs for a Server type in this Location |


# Example

```python
from hetznercloudapi.models.price_9 import Price9
from hetznercloudapi.models.price_hourly_8 import PriceHourly8
from hetznercloudapi.models.price_monthly_10 import PriceMonthly10

price_9 = Price9(
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
```



