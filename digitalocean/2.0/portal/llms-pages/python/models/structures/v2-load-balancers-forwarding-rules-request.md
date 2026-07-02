# V2 Load Balancers Forwarding Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMEZvcndhcmRpbmclMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2LoadBalancersForwardingRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `forwarding_rules` | [`List[ForwardingRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/forwarding-rule.md) | Required | **Constraints**: *Minimum Items*: `1` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.entry_protocol import EntryProtocol
from digitaloceanapi.models.forwarding_rule import ForwardingRule
from digitaloceanapi.models.target_protocol import TargetProtocol
from digitaloceanapi.models.v_2_load_balancers_forwarding_rules_request import V2LoadBalancersForwardingRulesRequest

v_2_load_balancers_forwarding_rules_request = V2LoadBalancersForwardingRulesRequest(
    forwarding_rules=[
        ForwardingRule(
            entry_port=443,
            entry_protocol=EntryProtocol.HTTPS,
            target_port=80,
            target_protocol=TargetProtocol.HTTP,
            certificate_id='892071a0-bb95-49bc-8021-3afd67a210bf',
            tls_passthrough=False,
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



