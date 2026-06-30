# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA


# Class Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apply_to` | [`List[ApplyTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the Firewall |
| `rules` | [`List[Rule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/rule.md) | Optional | Array of rules |


# Example

```python
import jsonpickle

from hetznercloudapi.models.apply_to import ApplyTo
from hetznercloudapi.models.create_firewall_request import CreateFirewallRequest
from hetznercloudapi.models.direction_enum import DirectionEnum
from hetznercloudapi.models.label_selector_1 import LabelSelector1
from hetznercloudapi.models.protocol_enum import ProtocolEnum
from hetznercloudapi.models.rule import Rule
from hetznercloudapi.models.server_2 import Server2
from hetznercloudapi.models.type_7_enum import Type7Enum

create_firewall_request = CreateFirewallRequest(
    name='Corporate Intranet Protection',
    apply_to=[
        ApplyTo(
            mtype=Type7Enum.SERVER,
            label_selector=LabelSelector1(
                selector='selector8'
            ),
            server=Server2(
                id=14
            )
        ),
        ApplyTo(
            mtype=Type7Enum.SERVER,
            label_selector=LabelSelector1(
                selector='selector8'
            ),
            server=Server2(
                id=14
            )
        ),
        ApplyTo(
            mtype=Type7Enum.SERVER,
            label_selector=LabelSelector1(
                selector='selector8'
            ),
            server=Server2(
                id=14
            )
        )
    ],
    labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    rules=[
        Rule(
            direction=DirectionEnum.ENUM_IN,
            protocol=ProtocolEnum.TCP,
            description='description2',
            destination_ips=[
                'destination_ips1',
                'destination_ips2',
                'destination_ips3'
            ],
            port='80',
            source_ips=[
                '28.239.13.1/32',
                '28.239.14.0/24',
                'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
            ]
        )
    ]
)
```



