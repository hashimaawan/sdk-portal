# Server Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Any.*


# Class Name

`ServerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server_type` | [`ServerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/server-type.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.cpu_type import CpuType
from hetznercloudapi.models.price_9 import Price9
from hetznercloudapi.models.price_hourly_8 import PriceHourly8
from hetznercloudapi.models.price_monthly_10 import PriceMonthly10
from hetznercloudapi.models.server_type import ServerType
from hetznercloudapi.models.server_types_response_1 import ServerTypesResponse1
from hetznercloudapi.models.storage_type import StorageType

server_types_response_1 = ServerTypesResponse1(
    server_type=ServerType(
        cores=1,
        cpu_type=CpuType.SHARED,
        deprecated=False,
        description='CX11',
        disk=24,
        id=1,
        memory=1,
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
        storage_type=StorageType.LOCAL,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



