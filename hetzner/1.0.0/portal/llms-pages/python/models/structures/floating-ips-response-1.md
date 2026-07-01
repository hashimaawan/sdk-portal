# Floating Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Any.*


# Class Name

`FloatingIpsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Optional | - |
| `floating_ip` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/floating-ip.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.action import Action
from hetznercloudapi.models.dns_ptr import DnsPtr
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.floating_ip import FloatingIp
from hetznercloudapi.models.floating_ips_response_1 import FloatingIpsResponse1
from hetznercloudapi.models.home_location import HomeLocation
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.status import Status
from hetznercloudapi.models.type_16 import Type16

floating_ips_response_1 = FloatingIpsResponse1(
    floating_ip=FloatingIp(
        blocked=False,
        created='2016-01-30T23:55:00+00:00',
        description='this describes my resource',
        dns_ptr=[
            DnsPtr(
                dns_ptr='server.example.com',
                ip='2001:db8::1',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        home_location=HomeLocation(
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
        id=42,
        ip='131.232.99.1',
        labels={
            'key0': 'labels4',
            'key1': 'labels3',
            'key2': 'labels2'
        },
        name='my-resource',
        protection=Protection(
            delete=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        server=42,
        mtype=Type16.IPV4,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    action=Action(
        command='command6',
        error=Error(
            code='code2',
            message='message4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        finished='finished0',
        id=238,
        progress=143.26,
        resources=[
            Resource(
                id=198,
                mtype='type0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Resource(
                id=198,
                mtype='type0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Resource(
                id=198,
                mtype='type0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        started='started8',
        status=Status.RUNNING,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



