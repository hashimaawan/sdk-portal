# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Any.*


# Class Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_type` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer-type.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.load_balancer_type import LoadBalancerType
from hetznercloudapi.models.load_balancer_types_response_1 import LoadBalancerTypesResponse1
from hetznercloudapi.models.price import Price
from hetznercloudapi.models.price_hourly import PriceHourly
from hetznercloudapi.models.price_monthly import PriceMonthly

load_balancer_types_response_1 = LoadBalancerTypesResponse1(
    load_balancer_type=LoadBalancerType(
        deprecated='deprecated2',
        description='description4',
        id=205.06,
        max_assigned_certificates=211.64,
        max_connections=136.32,
        max_services=199.18,
        max_targets=152.52,
        name='name6',
        prices=[
            Price(
                location='location8',
                price_hourly=PriceHourly(
                    gross='gross4',
                    net='net2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                price_monthly=PriceMonthly(
                    gross='gross2',
                    net='net0',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Price(
                location='location8',
                price_hourly=PriceHourly(
                    gross='gross4',
                    net='net2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                price_monthly=PriceMonthly(
                    gross='gross2',
                    net='net0',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Price(
                location='location8',
                price_hourly=PriceHourly(
                    gross='gross4',
                    net='net2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                price_monthly=PriceMonthly(
                    gross='gross2',
                    net='net0',
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
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



