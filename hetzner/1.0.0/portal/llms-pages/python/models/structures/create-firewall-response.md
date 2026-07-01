# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U

*This model accepts additional fields of type Any.*


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`List[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action.md) | Optional | - |
| `firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/firewall.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.action import Action
from hetznercloudapi.models.applied_to import AppliedTo
from hetznercloudapi.models.applied_to_resource import AppliedToResource
from hetznercloudapi.models.create_firewall_response import CreateFirewallResponse
from hetznercloudapi.models.direction import Direction
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.firewall import Firewall
from hetznercloudapi.models.label_selector import LabelSelector
from hetznercloudapi.models.protocol import Protocol
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.rule import Rule
from hetznercloudapi.models.server import Server
from hetznercloudapi.models.status import Status
from hetznercloudapi.models.type_5 import Type5
from hetznercloudapi.models.type_6 import Type6

create_firewall_response = CreateFirewallResponse(
    actions=[
        Action(
            command='set_firewall_rules',
            error=Error(
                code='action_failed',
                message='Action failed',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            finished='2016-01-30T23:56:00+00:00',
            id=13,
            progress=100,
            resources=[
                Resource(
                    id=38,
                    mtype='firewall',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            started='2016-01-30T23:55:00+00:00',
            status=Status.SUCCESS,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Action(
            command='apply_firewall',
            error=Error(
                code='action_failed',
                message='Action failed',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            finished='2016-01-30T23:56:00+00:00',
            id=14,
            progress=100,
            resources=[
                Resource(
                    id=42,
                    mtype='server',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                Resource(
                    id=38,
                    mtype='firewall',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            started='2016-01-30T23:55:00+00:00',
            status=Status.SUCCESS,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    firewall=Firewall(
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
            ),
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
        created='created6',
        id=4,
        name='name6',
        rules=[
            Rule(
                direction=Direction.ENUM_IN,
                protocol=Protocol.UDP,
                description='description2',
                destination_ips=[
                    'destination_ips1',
                    'destination_ips2',
                    'destination_ips3'
                ],
                port='port8',
                source_ips=[
                    'source_ips1',
                    'source_ips2',
                    'source_ips3'
                ],
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        labels={
            'key0': 'labels2',
            'key1': 'labels1'
        },
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



