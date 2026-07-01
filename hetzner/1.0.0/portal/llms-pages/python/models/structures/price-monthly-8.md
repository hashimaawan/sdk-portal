# Price Monthly 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTg

Monthly costs for a Load Balancer type in this network zone

*This model accepts additional fields of type Any.*


# Class Name

`PriceMonthly8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `str` | Required | Price with VAT added |
| `net` | `str` | Required | Price without VAT |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.price_monthly_8 import PriceMonthly8

price_monthly_8 = PriceMonthly8(
    gross='1.1900000000000000',
    net='1.0000000000',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



