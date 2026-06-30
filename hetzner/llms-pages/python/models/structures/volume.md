# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlZvbHVtZQ

The cost of Volume per GB/month


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_per_gb_month` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/price-per-gb-month.md) | Required | - |


# Example

```python
from hetznercloudapi.models.price_per_gb_month import PricePerGbMonth
from hetznercloudapi.models.volume import Volume

volume = Volume(
    price_per_gb_month=PricePerGbMonth(
        gross='1.1900000000000000',
        net='1.0000000000'
    )
)
```



