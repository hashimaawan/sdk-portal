# Price Monthly 10

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTEw

Monthly costs for a Server type in this Location


# Class Name

`PriceMonthly10`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |


# Example

```python
from hetznercloudapi.models.price_monthly_10 import PriceMonthly10

price_monthly_10 = PriceMonthly10(
    gross='1.1900000000000000',
    net='1.0000000000'
)
```



