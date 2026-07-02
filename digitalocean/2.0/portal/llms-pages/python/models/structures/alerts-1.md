# Alerts 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkFsZXJ0czE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Alerts1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Optional, Read-only | A unique ID that can be used to identify and reference the alert. |
| `comparison` | [`Comparison`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/comparison.md) | Optional | The comparison operator used against the alert's threshold. |
| `name` | `str` | Optional | A human-friendly display name. |
| `notifications` | [`Notifications`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/notifications.md) | Optional | The notification settings for a trigger alert. |
| `period` | [`Period`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/period.md) | Optional | Period of time the threshold must be exceeded to trigger the alert. |
| `threshold` | `int` | Optional | The threshold at which the alert will enter a trigger state. The specific threshold is dependent on the alert type. |
| `mtype` | [`Type20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-20.md) | Optional | The type of alert. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.alerts_1 import Alerts1
from digitaloceanapi.models.comparison import Comparison
from digitaloceanapi.models.notifications import Notifications
from digitaloceanapi.models.period import Period
from digitaloceanapi.models.slack import Slack
from digitaloceanapi.models.type_20 import Type20

alerts_1 = Alerts1(
    id='5a4981aa-9653-4bd1-bef5-d6bff52042e4',
    comparison=Comparison.GREATER_THAN,
    name='Landing page degraded performance',
    notifications=Notifications(
        email=[
            'email4',
            'email3'
        ],
        slack=[
            Slack(
                channel='channel6',
                url='url2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Slack(
                channel='channel6',
                url='url2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Slack(
                channel='channel6',
                url='url2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    period=Period.ENUM_2M,
    threshold=300,
    mtype=Type20.LATENCY,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



