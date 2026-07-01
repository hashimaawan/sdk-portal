# Set Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNldFJ1bGVzUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`SetRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rules` | [`List[Rule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/rule.md) | Required | Array of rules<br><br>**Constraints**: *Maximum Items*: `50` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.direction import Direction
from hetznercloudapi.models.protocol import Protocol
from hetznercloudapi.models.rule import Rule
from hetznercloudapi.models.set_rules_request import SetRulesRequest

set_rules_request = SetRulesRequest(
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
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



