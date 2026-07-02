# V2 Load Balancers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2LoadBalancersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer` | [`LoadBalancer1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/load-balancer-1.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.algorithm import Algorithm
from digitaloceanapi.models.entry_protocol import EntryProtocol
from digitaloceanapi.models.forwarding_rule import ForwardingRule
from digitaloceanapi.models.load_balancer_1 import LoadBalancer1
from digitaloceanapi.models.target_protocol import TargetProtocol
from digitaloceanapi.models.v_2_load_balancers_response_1 import V2LoadBalancersResponse1

v_2_load_balancers_response_1 = V2LoadBalancersResponse1(
    load_balancer=LoadBalancer1(
        forwarding_rules=[
            ForwardingRule(
                entry_port=220,
                entry_protocol=EntryProtocol.HTTP2,
                target_port=104,
                target_protocol=TargetProtocol.HTTPS,
                certificate_id='certificate_id4',
                tls_passthrough=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            ForwardingRule(
                entry_port=220,
                entry_protocol=EntryProtocol.HTTP2,
                target_port=104,
                target_protocol=TargetProtocol.HTTPS,
                certificate_id='certificate_id4',
                tls_passthrough=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        algorithm=Algorithm.ROUND_ROBIN,
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        disable_lets_encrypt_dns_records=False,
        enable_backend_keepalive=False,
        enable_proxy_protocol=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



