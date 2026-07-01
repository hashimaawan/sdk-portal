# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1

*This model accepts additional fields of type Any.*


# Class Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prices` | [`List[Price6]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-6.md) | Required | Floating IP type costs per Location |
| `mtype` | [`Type48`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-48.md) | Required | The type of the Floating IP |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.floating_ip_5 import FloatingIp5
from hetznercloudapi.models.price_6 import Price6
from hetznercloudapi.models.price_monthly_7 import PriceMonthly7
from hetznercloudapi.models.type_48 import Type48

floating_ip_5 = FloatingIp5(
    prices=[
        Price6(
            location='fsn1',
            price_monthly=PriceMonthly7(
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
    ],
    mtype=Type48.IPV4,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



