# Price

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNl

*This model accepts additional fields of type Any.*


# Class Name

`Price`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `str` | Required | Name of the Location the price is for |
| `price_hourly` | [`PriceHourly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-hourly.md) | Required | Hourly costs for a Resource in this Location |
| `price_monthly` | [`PriceMonthly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-monthly.md) | Required | Monthly costs for a Resource in this Location |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.price import Price
from hetznercloudapi.models.price_hourly import PriceHourly
from hetznercloudapi.models.price_monthly import PriceMonthly

price = Price(
    location='fsn1',
    price_hourly=PriceHourly(
        gross='1.1900000000000000',
        net='1.0000000000',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    price_monthly=PriceMonthly(
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



