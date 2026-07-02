# V2 Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBGbG9hdGluZyUyNTIwSXBzJTI1MjBBY3Rpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`List[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/action.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.action import Action
from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.region import Region
from digitaloceanapi.models.status_1 import Status1
from digitaloceanapi.models.v_2_floating_ips_actions_response import V2FloatingIpsActionsResponse

v_2_floating_ips_actions_response = V2FloatingIpsActionsResponse(
    meta=Meta(
        total=1,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    actions=[
        Action(
            completed_at=dateutil.parser.parse('2015-11-21T21:51:09Z'),
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
            resource_id=758604197,
            resource_type='floating_ip',
            started_at=dateutil.parser.parse('2015-11-21T21:51:09Z'),
            status=Status1.COMPLETED,
            mtype='reserve_ip',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    links=Links(
        pages=Pages(
            last='last6',
            next='next2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



