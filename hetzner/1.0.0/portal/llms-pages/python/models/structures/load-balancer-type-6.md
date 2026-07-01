# Load Balancer Type 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU2

*This model accepts additional fields of type Any.*


# Class Name

`LoadBalancerType6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `float` | Required | ID of the Load Balancer type the price is for |
| `name` | `str` | Required | Name of the Load Balancer type the price is for |
| `prices` | [`List[Price7]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-7.md) | Required | Load Balancer type costs per Location |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.load_balancer_type_6 import LoadBalancerType6
from hetznercloudapi.models.price_7 import Price7
from hetznercloudapi.models.price_hourly_6 import PriceHourly6
from hetznercloudapi.models.price_monthly_8 import PriceMonthly8

load_balancer_type_6 = LoadBalancerType6(
    id=1,
    name='lb11',
    prices=[
        Price7(
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
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



