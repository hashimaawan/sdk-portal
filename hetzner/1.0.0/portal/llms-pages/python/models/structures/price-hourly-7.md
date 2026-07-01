# Price Hourly 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNlSG91cmx5Nw

Hourly costs for a Primary IP type in this Location


# Class Name

`PriceHourly7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |


# Example

```python
from hetznercloudapi.models.price_hourly_7 import PriceHourly7

price_hourly_7 = PriceHourly7(
    gross='1.1900000000000000',
    net='1.0000000000'
)
```



