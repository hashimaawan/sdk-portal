# V2 Monitoring Alerts Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2MonitoringAlertsRequest`


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
| `value` | `float` | Required | - |
| `window` | [`Window1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/window-1.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.alerts import Alerts
from digitaloceanapi.models.compare import Compare
from digitaloceanapi.models.slack import Slack
from digitaloceanapi.models.type_17 import Type17
from digitaloceanapi.models.v_2_monitoring_alerts_request import V2MonitoringAlertsRequest
from digitaloceanapi.models.window_1 import Window1

v_2_monitoring_alerts_request = V2MonitoringAlertsRequest(
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
    value=80,
    window=Window1.ENUM_5M,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



