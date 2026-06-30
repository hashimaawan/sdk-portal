# Price Monthly

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlByaWNlTW9udGhseQ

Monthly costs for a Resource in this Location


# Class Name

`PriceMonthly`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |


# Example

```python
from hetznercloudapi.models.price_monthly import PriceMonthly

price_monthly = PriceMonthly(
    gross='1.1900000000000000',
    net='1.0000000000'
)
```



