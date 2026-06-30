# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkZpcmV3YWxs


# Class Name

`Firewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applied_to` | [`List[AppliedTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/applied-to.md) | Required | - |
| `created` | `str` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `int` | Required | ID of the Resource |
| `labels` | `Dict[str, str]` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the Resource. Must be unique per Project. |
| `rules` | [`List[Rule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/rule.md) | Required | - |


# Example

```python
from hetznercloudapi.models.applied_to import AppliedTo
from hetznercloudapi.models.applied_to_resource import AppliedToResource
from hetznercloudapi.models.direction_enum import DirectionEnum
from hetznercloudapi.models.firewall import Firewall
from hetznercloudapi.models.label_selector import LabelSelector
from hetznercloudapi.models.protocol_enum import ProtocolEnum
from hetznercloudapi.models.rule import Rule
from hetznercloudapi.models.server import Server
from hetznercloudapi.models.type_5_enum import Type5Enum
from hetznercloudapi.models.type_6_enum import Type6Enum

firewall = Firewall(
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
        )
    ],
    created='2016-01-30T23:55:00+00:00',
    id=42,
    name='my-resource',
    rules=[
        Rule(
            direction=DirectionEnum.ENUM_IN,
            protocol=ProtocolEnum.UDP,
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
            ]
        )
    ],
    labels={
        'key0': 'labels2',
        'key1': 'labels1'
    }
)
```



