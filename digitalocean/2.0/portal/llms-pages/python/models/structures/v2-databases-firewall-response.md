# V2 Databases Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMEZpcmV3YWxsJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rules` | [`List[Rule1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/rule-1.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.rule_1 import Rule1
from digitaloceanapi.models.type_7 import Type7
from digitaloceanapi.models.v_2_databases_firewall_response import V2DatabasesFirewallResponse

v_2_databases_firewall_response = V2DatabasesFirewallResponse(
    rules=[
        Rule1(
            mtype=Type7.IP_ADDR,
            value='value0',
            cluster_uuid='cluster_uuid4',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            uuid='uuid4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Rule1(
            mtype=Type7.IP_ADDR,
            value='value0',
            cluster_uuid='cluster_uuid4',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            uuid='uuid4',
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



