# Price 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNlNw

*This model accepts additional fields of type Any.*


# Class Name

`Price7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `str` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-hourly-6.md) | Required | Hourly costs for a Load Balancer type in this network zone |
| `price_monthly` | [`PriceMonthly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-monthly-8.md) | Required | Monthly costs for a Load Balancer type in this network zone |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.price_7 import Price7
from hetznercloudapi.models.price_hourly_6 import PriceHourly6
from hetznercloudapi.models.price_monthly_8 import PriceMonthly8

price_7 = Price7(
    location='fsn1',
    price_hourly=PriceHourly6(
        gross='1.1900000000000000',
        net='1.0000000000',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    price_monthly=PriceMonthly8(
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



