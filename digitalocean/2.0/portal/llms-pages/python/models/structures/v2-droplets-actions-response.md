# V2 Droplets Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DropletsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`List[Action]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/action.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.action import Action
from digitaloceanapi.models.region import Region
from digitaloceanapi.models.v_2_droplets_actions_response import V2DropletsActionsResponse

v_2_droplets_actions_response = V2DropletsActionsResponse(
    actions=[
        Action(
            completed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            id=154,
            region=Region(
                available=False,
                features=[
                    'features7',
                    'features8',
                    'features9'
                ],
                name='name6',
                sizes=[
                    'sizes6'
                ],
                slug='slug0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            region_slug='region_slug6',
            resource_id=238,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Action(
            completed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            id=154,
            region=Region(
                available=False,
                features=[
                    'features7',
                    'features8',
                    'features9'
                ],
                name='name6',
                sizes=[
                    'sizes6'
                ],
                slug='slug0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            region_slug='region_slug6',
            resource_id=238,
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



