# V2 Firewalls Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2FirewallsRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `inbound_rules` | [`List[InboundRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/inbound-rule.md) | Required | - |
| `outbound_rules` | [`List[OutboundRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/outbound-rule.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.destinations import Destinations
from digitaloceanapi.models.inbound_rule import InboundRule
from digitaloceanapi.models.outbound_rule import OutboundRule
from digitaloceanapi.models.protocol import Protocol
from digitaloceanapi.models.sources import Sources
from digitaloceanapi.models.v_2_firewalls_rules_request import V2FirewallsRulesRequest

v_2_firewalls_rules_request = V2FirewallsRulesRequest(
    inbound_rules=[
        InboundRule(
            ports='8000',
            protocol=Protocol.TCP,
            sources=Sources(
                addresses=[
                    '1.2.3.4',
                    '18.0.0.0/8'
                ],
                droplet_ids=[
                    8043964
                ],
                kubernetes_ids=[
                    '41b74c5d-9bd0-5555-5555-a57c495b81a3'
                ],
                load_balancer_uids=[
                    '4de7ac8b-495b-4884-9a69-1050c6793cd6'
                ],
                tags=[
                    'tags1',
                    'tags2',
                    'tags3'
                ],
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    outbound_rules=[
        OutboundRule(
            ports='8000',
            protocol=Protocol.TCP,
            destinations=Destinations(
                addresses=[
                    '1.2.3.4',
                    '18.0.0.0/8'
                ],
                droplet_ids=[
                    8043964
                ],
                kubernetes_ids=[
                    '41b74c5d-9bd0-5555-5555-a57c495b81a3'
                ],
                load_balancer_uids=[
                    '4de7ac8b-495b-4884-9a69-1050c6793cd6'
                ],
                tags=[
                    'tags7',
                    'tags8',
                    'tags9'
                ],
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
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



