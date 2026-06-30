# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_type` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/load-balancer-type.md) | Optional | - |


# Example

```python
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
                    net='net2'
                ),
                price_monthly=PriceMonthly(
                    gross='gross2',
                    net='net0'
                )
            ),
            Price(
                location='location8',
                price_hourly=PriceHourly(
                    gross='gross4',
                    net='net2'
                ),
                price_monthly=PriceMonthly(
                    gross='gross2',
                    net='net0'
                )
            ),
            Price(
                location='location8',
                price_hourly=PriceHourly(
                    gross='gross4',
                    net='net2'
                ),
                price_monthly=PriceMonthly(
                    gross='gross2',
                    net='net0'
                )
            )
        ]
    )
)
```



