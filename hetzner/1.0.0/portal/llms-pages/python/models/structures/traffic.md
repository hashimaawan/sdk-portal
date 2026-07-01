# Traffic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlRyYWZmaWM

The cost of additional traffic per TB

*This model accepts additional fields of type Any.*


# Class Name

`Traffic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_per_tb` | [`PricePerTb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-per-tb.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.price_per_tb import PricePerTb
from hetznercloudapi.models.traffic import Traffic

traffic = Traffic(
    price_per_tb=PricePerTb(
        gross='1.1900000000000000',
        net='1.0000000000',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



