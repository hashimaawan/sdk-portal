# Price Monthly 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTY


# Class Name

`PriceMonthly6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |


# Example

```python
from hetznercloudapi.models.price_monthly_6 import PriceMonthly6

price_monthly_6 = PriceMonthly6(
    gross='1.1900000000000000',
    net='1.0000000000'
)
```



