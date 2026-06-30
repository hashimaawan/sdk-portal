# API Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRkFQSVJlcXVlc3Q

Represents a request that was made to the API. Including what Token was used and what resource was accessed.

*This model accepts additional fields of type Any.*


# Class Name

`ApiRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/enumerations/action.md) | Optional | - |
| `actor` | [`Actor`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/actor.md) | Optional | - |
| `request_id` | `uuid\|str` | Optional | The unique id used to identify a single request. |
| `resource` | [`Resource`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/resource.md) | Optional | - |
| `result` | [`Result`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/enumerations/result.md) | Optional | - |
| `timestamp` | `datetime` | Optional, Read-only | The time at which the request was processed by the server. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.action import Action
from m1passwordconnect.models.actor import Actor
from m1passwordconnect.models.api_request import ApiRequest
from m1passwordconnect.models.item_2 import Item2
from m1passwordconnect.models.mtype import Type
from m1passwordconnect.models.resource import Resource
from m1passwordconnect.models.result import Result
from m1passwordconnect.models.vault_3 import Vault3

api_request = ApiRequest(
    action=Action.UPDATE,
    actor=Actor(
        account='account0',
        id='0000193c-0000-0000-0000-000000000000',
        jti='jti2',
        request_ip='requestIp4',
        user_agent='userAgent6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    request_id='0000206a-0000-0000-0000-000000000000',
    resource=Resource(
        item=Item2(
            id='id2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        item_version=108,
        mtype=Type.ITEM,
        vault=Vault3(
            id='id6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    result=Result.SUCCESS,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



