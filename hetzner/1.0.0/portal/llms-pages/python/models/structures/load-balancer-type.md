# Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU

*This model accepts additional fields of type Any.*


# Class Name

`LoadBalancerType`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deprecated` | `str` | Required | Point in time when the Load Balancer type is deprecated (in ISO-8601 format) |
| `description` | `str` | Required | Description of the Load Balancer type |
| `id` | `float` | Required | ID of the Load Balancer type |
| `max_assigned_certificates` | `float` | Required | Number of SSL Certificates that can be assigned to a single Load Balancer |
| `max_connections` | `float` | Required | Number of maximum simultaneous open connections |
| `max_services` | `float` | Required | Number of services a Load Balancer of this type can have |
| `max_targets` | `float` | Required | Number of targets a single Load Balancer can have |
| `name` | `str` | Required | Unique identifier of the Load Balancer type |
| `prices` | [`List[Price]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price.md) | Required | Prices in different network zones |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.load_balancer_type import LoadBalancerType
from hetznercloudapi.models.price import Price
from hetznercloudapi.models.price_hourly import PriceHourly
from hetznercloudapi.models.price_monthly import PriceMonthly

load_balancer_type = LoadBalancerType(
    deprecated='2016-01-30T23:50:00+00:00',
    description='LB11',
    id=1,
    max_assigned_certificates=10,
    max_connections=20000,
    max_services=5,
    max_targets=25,
    name='lb11',
    prices=[
        Price(
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
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



