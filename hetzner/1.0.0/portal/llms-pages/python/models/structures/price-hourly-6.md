# Price Hourly 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNlSG91cmx5Ng

Hourly costs for a Load Balancer type in this network zone


# Class Name

`PriceHourly6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |


# Example

```python
from hetznercloudapi.models.price_hourly_6 import PriceHourly6

price_hourly_6 = PriceHourly6(
    gross='1.1900000000000000',
    net='1.0000000000'
)
```



