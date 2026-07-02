# V2 Reserved Ips Actions Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBBY3Rpb25zJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2ReservedIpsActionsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/action-2.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.action_2 import Action2
from digitaloceanapi.models.region import Region
from digitaloceanapi.models.status_1 import Status1
from digitaloceanapi.models.v_2_reserved_ips_actions_response_1 import V2ReservedIpsActionsResponse1

v_2_reserved_ips_actions_response_1 = V2ReservedIpsActionsResponse1(
    action=Action2(
        completed_at=dateutil.parser.parse('2015-11-12T17:51:14Z'),
        id=72531856,
        region=Region(
            available=True,
            features=[
                'private_networking',
                'backups',
                'ipv6',
                'metadata'
            ],
            name='New York 3',
            sizes=[
                's-1vcpu-1gb',
                's-1vcpu-2gb',
                's-1vcpu-3gb',
                's-2vcpu-2gb',
                's-3vcpu-1gb',
                's-2vcpu-4gb',
                's-4vcpu-8gb',
                's-6vcpu-16gb',
                's-8vcpu-32gb',
                's-12vcpu-48gb',
                's-16vcpu-64gb',
                's-20vcpu-96gb',
                's-24vcpu-128gb',
                's-32vcpu-192gb'
            ],
            slug='nyc3',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        region_slug='nyc3',
        resource_id=758604968,
        resource_type='reserved_ip',
        started_at=dateutil.parser.parse('2015-11-12T17:51:03Z'),
        status=Status1.COMPLETED,
        mtype='assign_ip',
        project_id='746c6152-2fa2-11ed-92d3-27aaa54e4988',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



