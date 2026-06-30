# Load Balancer Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2U


# Class Name

`LoadBalancerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_types` | [`List[LoadBalancerType]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/load-balancer-type.md) | Required | - |


# Example

```python
from hetznercloudapi.models.load_balancer_type import LoadBalancerType
from hetznercloudapi.models.load_balancer_types_response import LoadBalancerTypesResponse
from hetznercloudapi.models.price import Price
from hetznercloudapi.models.price_hourly import PriceHourly
from hetznercloudapi.models.price_monthly import PriceMonthly

load_balancer_types_response = LoadBalancerTypesResponse(
    load_balancer_types=[
        LoadBalancerType(
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
                        net='1.0000000000'
                    ),
                    price_monthly=PriceMonthly(
                        gross='1.1900000000000000',
                        net='1.0000000000'
                    )
                )
            ]
        )
    ]
)
```



