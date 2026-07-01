# Floating Ip 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA0

The cost of one Floating IP per month


# Class Name

`FloatingIp4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_monthly` | [`PriceMonthly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-monthly-6.md) | Required | - |


# Example

```python
from hetznercloudapi.models.floating_ip_4 import FloatingIp4
from hetznercloudapi.models.price_monthly_6 import PriceMonthly6

floating_ip_4 = FloatingIp4(
    price_monthly=PriceMonthly6(
        gross='1.1900000000000000',
        net='1.0000000000'
    )
)
```



