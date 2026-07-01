# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `apply_to` | [`List[ApplyTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the Firewall |
| `rules` | [`List[Rule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/rule.md) | Optional | Array of rules |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.apply_to import ApplyTo
from hetznercloudapi.models.create_firewall_request import CreateFirewallRequest
from hetznercloudapi.models.direction import Direction
from hetznercloudapi.models.label_selector_1 import LabelSelector1
from hetznercloudapi.models.protocol import Protocol
from hetznercloudapi.models.rule import Rule
from hetznercloudapi.models.server_2 import Server2
from hetznercloudapi.models.type_7 import Type7

create_firewall_request = CreateFirewallRequest(
    name='Corporate Intranet Protection',
    apply_to=[
        ApplyTo(
            mtype=Type7.SERVER,
            label_selector=LabelSelector1(
                selector='selector8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            server=Server2(
                id=14,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ApplyTo(
            mtype=Type7.SERVER,
            label_selector=LabelSelector1(
                selector='selector8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            server=Server2(
                id=14,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ApplyTo(
            mtype=Type7.SERVER,
            label_selector=LabelSelector1(
                selector='selector8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            server=Server2(
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
    labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    rules=[
        Rule(
            direction=Direction.ENUM_IN,
            protocol=Protocol.TCP,
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
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



