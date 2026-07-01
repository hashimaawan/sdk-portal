# Price Hourly 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNlSG91cmx5OA

Hourly costs for a Server type in this Location

*This model accepts additional fields of type Any.*


# Class Name

`PriceHourly8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.price_hourly_8 import PriceHourly8

price_hourly_8 = PriceHourly8(
    gross='1.1900000000000000',
    net='1.0000000000',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



