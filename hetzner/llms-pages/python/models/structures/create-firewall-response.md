# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`List[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/action.md) | Optional | - |
| `firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/firewall.md) | Optional | - |


# Example

```python
from hetznercloudapi.models.action import Action
from hetznercloudapi.models.applied_to import AppliedTo
from hetznercloudapi.models.applied_to_resource import AppliedToResource
from hetznercloudapi.models.create_firewall_response import CreateFirewallResponse
from hetznercloudapi.models.direction_enum import DirectionEnum
from hetznercloudapi.models.error import Error
from hetznercloudapi.models.firewall import Firewall
from hetznercloudapi.models.label_selector import LabelSelector
from hetznercloudapi.models.protocol_enum import ProtocolEnum
from hetznercloudapi.models.resource import Resource
from hetznercloudapi.models.rule import Rule
from hetznercloudapi.models.server import Server
from hetznercloudapi.models.status_enum import StatusEnum
from hetznercloudapi.models.type_5_enum import Type5Enum
from hetznercloudapi.models.type_6_enum import Type6Enum

create_firewall_response = CreateFirewallResponse(
    actions=[
        Action(
            command='set_firewall_rules',
            error=Error(
                code='action_failed',
                message='Action failed'
            ),
            finished='2016-01-30T23:56:00+00:00',
            id=13,
            progress=100,
            resources=[
                Resource(
                    id=38,
                    mtype='firewall'
                )
            ],
            started='2016-01-30T23:55:00+00:00',
            status=StatusEnum.SUCCESS
        ),
        Action(
            command='apply_firewall',
            error=Error(
                code='action_failed',
                message='Action failed'
            ),
            finished='2016-01-30T23:56:00+00:00',
            id=14,
            progress=100,
            resources=[
                Resource(
                    id=42,
                    mtype='server'
                ),
                Resource(
                    id=38,
                    mtype='firewall'
                )
            ],
            started='2016-01-30T23:55:00+00:00',
            status=StatusEnum.SUCCESS
        )
    ],
    firewall=Firewall(
        applied_to=[
            AppliedTo(
                mtype=Type6Enum.SERVER,
                applied_to_resources=[
                    AppliedToResource(
                        server=Server(
                            id=14
                        ),
                        mtype=Type5Enum.SERVER
                    )
                ],
                label_selector=LabelSelector(
                    selector='selector8'
                ),
                server=Server(
                    id=14
                )
            ),
            AppliedTo(
                mtype=Type6Enum.SERVER,
                applied_to_resources=[
                    AppliedToResource(
                        server=Server(
                            id=14
                        ),
                        mtype=Type5Enum.SERVER
                    )
                ],
                label_selector=LabelSelector(
                    selector='selector8'
                ),
                server=Server(
                    id=14
                )
            )
        ],
        created='created6',
        id=4,
        name='name6',
        rules=[
            Rule(
                direction=DirectionEnum.ENUM_IN,
                protocol=ProtocolEnum.UDP,
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
                ]
            )
        ],
        labels={
            'key0': 'labels2',
            'key1': 'labels1'
        }
    )
)
```



