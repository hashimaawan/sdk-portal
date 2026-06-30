# Price 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlByaWNlNw


# Class Name

`Price7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `str` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/price-hourly-6.md) | Required | Hourly costs for a Load Balancer type in this network zone |
| `price_monthly` | [`PriceMonthly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/price-monthly-8.md) | Required | Monthly costs for a Load Balancer type in this network zone |


# Example

```python
from hetznercloudapi.models.price_7 import Price7
from hetznercloudapi.models.price_hourly_6 import PriceHourly6
from hetznercloudapi.models.price_monthly_8 import PriceMonthly8

price_7 = Price7(
    location='fsn1',
    price_hourly=PriceHourly6(
        gross='1.1900000000000000',
        net='1.0000000000'
    ),
    price_monthly=PriceMonthly8(
        gross='1.1900000000000000',
        net='1.0000000000'
    )
)
```



