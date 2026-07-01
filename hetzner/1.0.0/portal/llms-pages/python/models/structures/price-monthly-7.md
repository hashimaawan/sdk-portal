# Price Monthly 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTc

Monthly costs for a Floating IP type in this Location


# Class Name

`PriceMonthly7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |


# Example

```python
from hetznercloudapi.models.price_monthly_7 import PriceMonthly7

price_monthly_7 = PriceMonthly7(
    gross='1.1900000000000000',
    net='1.0000000000'
)
```



