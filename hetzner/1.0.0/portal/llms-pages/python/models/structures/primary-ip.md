# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaW1hcnlJcA

*This model accepts additional fields of type Any.*


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prices` | [`List[Price8]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/price-8.md) | Required | Primary IP type costs per Location |
| `mtype` | [`Type49`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-49.md) | Required | The type of the Primary IP |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.price_8 import Price8
from hetznercloudapi.models.price_hourly_7 import PriceHourly7
from hetznercloudapi.models.price_monthly_9 import PriceMonthly9
from hetznercloudapi.models.primary_ip import PrimaryIp
from hetznercloudapi.models.type_49 import Type49

primary_ip = PrimaryIp(
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
```



