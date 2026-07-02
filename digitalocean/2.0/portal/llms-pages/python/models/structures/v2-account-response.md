# V2 Account Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBY2NvdW50JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AccountResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account` | [`Account`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/account.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.account import Account
from digitaloceanapi.models.status import Status
from digitaloceanapi.models.team import Team
from digitaloceanapi.models.v_2_account_response import V2AccountResponse

v_2_account_response = V2AccountResponse(
    account=Account(
        droplet_limit=248,
        email='email6',
        email_verified=False,
        floating_ip_limit=164,
        status=Status.WARNING,
        status_message='status_message8',
        uuid='uuid6',
        team=Team(
            name='name0',
            uuid='uuid6',
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



