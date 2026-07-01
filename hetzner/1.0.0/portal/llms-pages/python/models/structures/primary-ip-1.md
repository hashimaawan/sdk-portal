# Primary IP 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByaW1hcnlJUDE

*This model accepts additional fields of type Any.*


# Class Name

`PrimaryIp1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee_id` | `int` | Required | ID of the resource the Primary IP is assigned to, null if it is not assigned at all |
| `assignee_type` | `str` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `"server"` |
| `auto_delete` | `bool` | Required | Delete this Primary IP when the resource it is assigned to is deleted |
| `blocked` | `bool` | Required | Whether the IP is blocked |
| `created` | `str` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `datacenter` | [`Datacenter2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/datacenter-2.md) | Required | Datacenter this Primary IP is located at |
| `dns_ptr` | [`List[DnsPtr]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `id` | `int` | Required | ID of the Resource |
| `ip` | `str` | Required | IP address |
| `labels` | `Dict[str, str]` | Required | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the Resource. Must be unique per Project. |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `mtype` | [`Type50`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-50.md) | Required | Type of the Primary IP |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.datacenter_2 import Datacenter2
from hetznercloudapi.models.dns_ptr import DnsPtr
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.primary_ip_1 import PrimaryIp1
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.server_types import ServerTypes
from hetznercloudapi.models.type_50 import Type50

primary_ip_1 = PrimaryIp1(
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
        'key0': 'labels6'
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
)
```



