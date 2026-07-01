# Traffic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlRyYWZmaWM

The cost of additional traffic per TB


# Class Name

`Traffic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_per_tb` | [`PricePerTb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-per-tb.md) | Required | - |


# Example

```python
from hetznercloudapi.models.price_per_tb import PricePerTb
from hetznercloudapi.models.traffic import Traffic

traffic = Traffic(
    price_per_tb=PricePerTb(
        gross='1.1900000000000000',
        net='1.0000000000'
    )
)
```



