# Price 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNlNg


# Class Name

`Price6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `str` | Required | Name of the Location the price is for |
| `price_monthly` | [`PriceMonthly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-monthly-7.md) | Required | Monthly costs for a Floating IP type in this Location |


# Example

```python
from hetznercloudapi.models.price_6 import Price6
from hetznercloudapi.models.price_monthly_7 import PriceMonthly7

price_6 = Price6(
    location='fsn1',
    price_monthly=PriceMonthly7(
        gross='1.1900000000000000',
        net='1.0000000000'
    )
)
```



