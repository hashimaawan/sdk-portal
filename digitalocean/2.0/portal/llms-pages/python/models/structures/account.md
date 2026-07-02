# Account

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkFjY291bnQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Account`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet_limit` | `int` | Required | The total number of Droplets current user or team may have active at one time. |
| `email` | `str` | Required | The email address used by the current user to register for DigitalOcean. |
| `email_verified` | `bool` | Required | If true, the user has verified their account via email. False otherwise.<br><br>**Default**: `False` |
| `floating_ip_limit` | `int` | Required | The total number of Floating IPs the current user or team may have. |
| `status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status.md) | Required | This value is one of "active", "warning" or "locked".<br><br>**Default**: `"active"` |
| `status_message` | `str` | Required | A human-readable message giving more details about the status of the account. |
| `team` | [`Team`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/team.md) | Optional | When authorized in a team context, includes information about the current team. |
| `uuid` | `str` | Required | The unique universal identifier for the current user. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.account import Account
from digitaloceanapi.models.status import Status
from digitaloceanapi.models.team import Team

account = Account(
    droplet_limit=25,
    email='sammy@digitalocean.com',
    email_verified=True,
    floating_ip_limit=5,
    status=Status.ACTIVE,
    status_message=' ',
    uuid='b6fr89dbf6d9156cace5f3c78dc9851d957381ef',
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
)
```



