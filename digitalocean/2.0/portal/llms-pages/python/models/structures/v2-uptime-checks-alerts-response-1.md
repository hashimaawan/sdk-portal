# V2 Uptime Checks Alerts Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwQWxlcnRzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2UptimeChecksAlertsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alert` | [`Alerts1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/alerts-1.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.alerts_1 import Alerts1
from digitaloceanapi.models.comparison import Comparison
from digitaloceanapi.models.notifications import Notifications
from digitaloceanapi.models.period import Period
from digitaloceanapi.models.slack import Slack
from digitaloceanapi.models.v_2_uptime_checks_alerts_response_1 import V2UptimeChecksAlertsResponse1

v_2_uptime_checks_alerts_response_1 = V2UptimeChecksAlertsResponse1(
    alert=Alerts1(
        id='00002454-0000-0000-0000-000000000000',
        comparison=Comparison.GREATER_THAN,
        name='name0',
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
        period=Period.ENUM_30M,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



