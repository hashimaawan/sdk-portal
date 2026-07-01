# Price Hourly

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNlSG91cmx5

Hourly costs for a Resource in this Location


# Class Name

`PriceHourly`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |


# Example

```python
from hetznercloudapi.models.price_hourly import PriceHourly

price_hourly = PriceHourly(
    gross='1.1900000000000000',
    net='1.0000000000'
)
```



