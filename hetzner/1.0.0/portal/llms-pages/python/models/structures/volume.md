# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlZvbHVtZQ

The cost of Volume per GB/month

*This model accepts additional fields of type Any.*


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_per_gb_month` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-per-gb-month.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.price_per_gb_month import PricePerGbMonth
from hetznercloudapi.models.volume import Volume

volume = Volume(
    price_per_gb_month=PricePerGbMonth(
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



