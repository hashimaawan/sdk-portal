# Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaW1hcnlJUFJlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`PrimaryIpResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `primary_ip` | [`PrimaryIp1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/primary-ip-1.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.datacenter_2 import Datacenter2
from hetznercloudapi.models.dns_ptr import DnsPtr
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.primary_ip_1 import PrimaryIp1
from hetznercloudapi.models.primary_ip_response import PrimaryIpResponse
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.server_types import ServerTypes
from hetznercloudapi.models.type_50 import Type50

primary_ip_response = PrimaryIpResponse(
    primary_ip=PrimaryIp1(
        assignee_id=17,
        auto_delete=True,
        blocked=False,
        created='2016-01-30T23:55:00+00:00',
        datacenter=Datacenter2(
            description='Falkenstein DC Park 8',
            id=42,
            location=Location(
                city='Falkenstein',
                country='DE',
                description='Falkenstein DC Park 1',
                id=1,
                latitude=50.47612,
                longitude=12.370071,
                name='fsn1',
                network_zone='eu-central',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            name='fsn1-dc8',
            server_types=ServerTypes(
                available=[
                    1,
                    2,
                    3
                ],
                available_for_migration=[
                    1,
                    2,
                    3
                ],
                supported=[
                    1,
                    2,
                    3
                ],
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        dns_ptr=[
            DnsPtr(
                dns_ptr='server.example.com',
                ip='2001:db8::1',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        id=42,
        ip='131.232.99.1',
        labels={
            'key0': 'labels2',
            'key1': 'labels1'
        },
        name='my-resource',
        protection=Protection(
            delete=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        mtype=Type50.IPV4,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



