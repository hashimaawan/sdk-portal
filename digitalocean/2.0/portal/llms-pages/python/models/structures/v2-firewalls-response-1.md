# V2 Firewalls Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2FirewallsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/firewall.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.firewall import Firewall
from digitaloceanapi.models.pending_change import PendingChange
from digitaloceanapi.models.v_2_firewalls_response_1 import V2FirewallsResponse1

v_2_firewalls_response_1 = V2FirewallsResponse1(
    firewall=Firewall(
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        droplet_ids=[
            67
        ],
        id='id6',
        name='name6',
        pending_changes=[
            None,
            PendingChange(),
            PendingChange()
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



