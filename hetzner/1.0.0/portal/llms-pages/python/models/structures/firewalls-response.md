# Firewalls Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkZpcmV3YWxsc1Jlc3BvbnNl

*This model accepts additional fields of type Any.*


# Class Name

`FirewallsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewalls` | [`List[Firewall]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/firewall.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/meta.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.applied_to import AppliedTo
from hetznercloudapi.models.applied_to_resource import AppliedToResource
from hetznercloudapi.models.direction import Direction
from hetznercloudapi.models.firewall import Firewall
from hetznercloudapi.models.firewalls_response import FirewallsResponse
from hetznercloudapi.models.label_selector import LabelSelector
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.protocol import Protocol
from hetznercloudapi.models.rule import Rule
from hetznercloudapi.models.server import Server
from hetznercloudapi.models.type_5 import Type5
from hetznercloudapi.models.type_6 import Type6

firewalls_response = FirewallsResponse(
    firewalls=[
        Firewall(
            applied_to=[
                AppliedTo(
                    mtype=Type6.SERVER,
                    applied_to_resources=[
                        AppliedToResource(
                            server=Server(
                                id=14,
                                additional_properties={
                                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                                }
                            ),
                            mtype=Type5.SERVER,
                            additional_properties={
                                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                            }
                        )
                    ],
                    label_selector=LabelSelector(
                        selector='selector8',
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    server=Server(
                        id=14,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            created='2016-01-30T23:55:00+00:00',
            id=42,
            name='my-resource',
            rules=[
                Rule(
                    direction=Direction.ENUM_IN,
                    protocol=Protocol.UDP,
                    description='description2',
                    destination_ips=[
                        '28.239.13.1/32',
                        '28.239.14.0/24',
                        'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
                    ],
                    port='80',
                    source_ips=[
                        '28.239.13.1/32',
                        '28.239.14.0/24',
                        'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
                    ],
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            labels={
                'key0': 'labels4',
                'key1': 'labels5'
            },
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



