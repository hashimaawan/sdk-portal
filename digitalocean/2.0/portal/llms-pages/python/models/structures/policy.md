# Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlBvbGljeQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Policy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alerts` | [`Alerts`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/alerts.md) | Required | - |
| `compare` | [`Compare`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/compare.md) | Required | - |
| `description` | `str` | Required | - |
| `enabled` | `bool` | Required | - |
| `entities` | `List[str]` | Required | - |
| `tags` | `List[str]` | Required | - |
| `mtype` | [`Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-17.md) | Required | - |
| `uuid` | `str` | Required | - |
| `value` | `float` | Required | - |
| `window` | [`Window1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/window-1.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.alerts import Alerts
from digitaloceanapi.models.compare import Compare
from digitaloceanapi.models.policy import Policy
from digitaloceanapi.models.slack import Slack
from digitaloceanapi.models.type_17 import Type17
from digitaloceanapi.models.window_1 import Window1

policy = Policy(
    alerts=Alerts(
        email=[
            'bob@exmaple.com'
        ],
        slack=[
            Slack(
                channel='Production Alerts',
                url='https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    compare=Compare.GREATERTHAN,
    description='CPU Alert',
    enabled=True,
    entities=[
        '192018292'
    ],
    tags=[
        'droplet_tag'
    ],
    mtype=Type17.ENUM_V1INSIGHTSDROPLETCPU,
    uuid='78b3da62-27e5-49ba-ac70-5db0b5935c64',
    value=80,
    window=Window1.ENUM_5M,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



