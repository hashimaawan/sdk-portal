# Price per Gb Month

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNlUGVyR2JNb250aA


# Class Name

`PricePerGbMonth`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |


# Example

```python
from hetznercloudapi.models.price_per_gb_month import PricePerGbMonth

price_per_gb_month = PricePerGbMonth(
    gross='1.1900000000000000',
    net='1.0000000000'
)
```



