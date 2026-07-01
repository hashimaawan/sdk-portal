# Image 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkltYWdlMw

The cost of Image per GB/month


# Class Name

`Image3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_per_gb_month` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-per-gb-month.md) | Required | - |


# Example

```python
from hetznercloudapi.models.image_3 import Image3
from hetznercloudapi.models.price_per_gb_month import PricePerGbMonth

image_3 = Image3(
    price_per_gb_month=PricePerGbMonth(
        gross='1.1900000000000000',
        net='1.0000000000'
    )
)
```



