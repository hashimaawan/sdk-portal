# Pricing Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNpbmclMjUyMFJlc3BvbnNl


# Class Name

`PricingResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pricing` | [`Pricing`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/pricing.md) | Required | - |


# Example

```python
from hetznercloudapi.models.floating_ip_4 import FloatingIp4
from hetznercloudapi.models.floating_ip_5 import FloatingIp5
from hetznercloudapi.models.image_3 import Image3
from hetznercloudapi.models.load_balancer_type_6 import LoadBalancerType6
from hetznercloudapi.models.price_6 import Price6
from hetznercloudapi.models.price_7 import Price7
from hetznercloudapi.models.price_8 import Price8
from hetznercloudapi.models.price_9 import Price9
from hetznercloudapi.models.price_hourly_6 import PriceHourly6
from hetznercloudapi.models.price_hourly_7 import PriceHourly7
from hetznercloudapi.models.price_hourly_8 import PriceHourly8
from hetznercloudapi.models.price_monthly_10 import PriceMonthly10
from hetznercloudapi.models.price_monthly_6 import PriceMonthly6
from hetznercloudapi.models.price_monthly_7 import PriceMonthly7
from hetznercloudapi.models.price_monthly_8 import PriceMonthly8
from hetznercloudapi.models.price_monthly_9 import PriceMonthly9
from hetznercloudapi.models.price_per_gb_month import PricePerGbMonth
from hetznercloudapi.models.price_per_tb import PricePerTb
from hetznercloudapi.models.pricing import Pricing
from hetznercloudapi.models.pricing_response import PricingResponse
from hetznercloudapi.models.primary_ip import PrimaryIp
from hetznercloudapi.models.server_backup import ServerBackup
from hetznercloudapi.models.server_types_2 import ServerTypes2
from hetznercloudapi.models.traffic import Traffic
from hetznercloudapi.models.type_48_enum import Type48Enum
from hetznercloudapi.models.type_49_enum import Type49Enum
from hetznercloudapi.models.volume import Volume

pricing_response = PricingResponse(
    pricing=Pricing(
        currency='EUR',
        floating_ip=FloatingIp4(
            price_monthly=PriceMonthly6(
                gross='1.1900000000000000',
                net='1.0000000000'
            )
        ),
        floating_ips=[
            FloatingIp5(
                prices=[
                    Price6(
                        location='fsn1',
                        price_monthly=PriceMonthly7(
                            gross='1.1900000000000000',
                            net='1.0000000000'
                        )
                    )
                ],
                mtype=Type48Enum.IPV4
            )
        ],
        image=Image3(
            price_per_gb_month=PricePerGbMonth(
                gross='1.1900000000000000',
                net='1.0000000000'
            )
        ),
        load_balancer_types=[
            LoadBalancerType6(
                id=1,
                name='lb11',
                prices=[
                    Price7(
                        location='fsn1',
                        price_hourly=PriceHourly6(
                            gross='1.1900000000000000',
                            net='1.0000000000'
                        ),
                        price_monthly=PriceMonthly8(
                            gross='1.1900000000000000',
                            net='1.0000000000'
                        )
                    )
                ]
            )
        ],
        primary_ips=[
            PrimaryIp(
                prices=[
                    Price8(
                        location='fsn1',
                        price_hourly=PriceHourly7(
                            gross='1.1900000000000000',
                            net='1.0000000000'
                        ),
                        price_monthly=PriceMonthly9(
                            gross='1.1900000000000000',
                            net='1.0000000000'
                        )
                    )
                ],
                mtype=Type49Enum.IPV4
            )
        ],
        server_backup=ServerBackup(
            percentage='20.0000000000'
        ),
        server_types=[
            ServerTypes2(
                id=4,
                name='cx11',
                prices=[
                    Price9(
                        location='fsn1',
                        price_hourly=PriceHourly8(
                            gross='1.1900000000000000',
                            net='1.0000000000'
                        ),
                        price_monthly=PriceMonthly10(
                            gross='1.1900000000000000',
                            net='1.0000000000'
                        )
                    )
                ]
            )
        ],
        traffic=Traffic(
            price_per_tb=PricePerTb(
                gross='1.1900000000000000',
                net='1.0000000000'
            )
        ),
        vat_rate='19.000000',
        volume=Volume(
            price_per_gb_month=PricePerGbMonth(
                gross='1.1900000000000000',
                net='1.0000000000'
            )
        )
    )
)
```



