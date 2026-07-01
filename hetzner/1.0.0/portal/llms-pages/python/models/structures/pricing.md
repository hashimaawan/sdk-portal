# Pricing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaWNpbmc


# Class Name

`Pricing`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currency` | `str` | Required | Currency the returned prices are expressed in, coded according to ISO 4217 |
| `floating_ip` | [`FloatingIp4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/floating-ip-4.md) | Required | The cost of one Floating IP per month |
| `floating_ips` | [`List[FloatingIp5]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/floating-ip-5.md) | Required | Costs of Floating IPs types per Location and type |
| `image` | [`Image3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/image-3.md) | Required | The cost of Image per GB/month |
| `load_balancer_types` | [`List[LoadBalancerType6]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer-type-6.md) | Required | Costs of Load Balancer types per Location and type |
| `primary_ips` | [`List[PrimaryIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/primary-ip.md) | Required | Costs of Primary IPs types per Location |
| `server_backup` | [`ServerBackup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-backup.md) | Required | Will increase base Server costs by specific percentage |
| `server_types` | [`List[ServerTypes2]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-types-2.md) | Required | Costs of Server types per Location and type |
| `traffic` | [`Traffic`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/traffic.md) | Required | The cost of additional traffic per TB |
| `vat_rate` | `str` | Required | The VAT rate used for calculating prices with VAT |
| `volume` | [`Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/volume.md) | Required | The cost of Volume per GB/month |


# Example

```python
import jsonpickle

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
from hetznercloudapi.models.primary_ip import PrimaryIp
from hetznercloudapi.models.server_backup import ServerBackup
from hetznercloudapi.models.server_types_2 import ServerTypes2
from hetznercloudapi.models.traffic import Traffic
from hetznercloudapi.models.type_48 import Type48
from hetznercloudapi.models.type_49 import Type49
from hetznercloudapi.models.volume import Volume

pricing = Pricing(
    currency='EUR',
    floating_ip=FloatingIp4(
        price_monthly=PriceMonthly6(
            gross='1.1900000000000000',
            net='1.0000000000',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    floating_ips=[
        FloatingIp5(
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
    ],
    image=Image3(
        price_per_gb_month=PricePerGbMonth(
            gross='1.1900000000000000',
            net='1.0000000000',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
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
    ],
    primary_ips=[
        PrimaryIp(
            prices=[
                Price8(
                    location='fsn1',
                    price_hourly=PriceHourly7(
                        gross='1.1900000000000000',
                        net='1.0000000000',
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    price_monthly=PriceMonthly9(
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
            mtype=Type49.IPV4,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    server_backup=ServerBackup(
        percentage='20.0000000000',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
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
                        net='1.0000000000',
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    price_monthly=PriceMonthly10(
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
    ],
    traffic=Traffic(
        price_per_tb=PricePerTb(
            gross='1.1900000000000000',
            net='1.0000000000',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    vat_rate='19.000000',
    volume=Volume(
        price_per_gb_month=PricePerGbMonth(
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
)
```



