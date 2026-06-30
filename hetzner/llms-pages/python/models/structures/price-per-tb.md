# Price per Tb

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlByaWNlUGVyVGI


# Class Name

`PricePerTb`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |


# Example

```python
from hetznercloudapi.models.price_per_tb import PricePerTb

price_per_tb = PricePerTb(
    gross='1.1900000000000000',
    net='1.0000000000'
)
```



