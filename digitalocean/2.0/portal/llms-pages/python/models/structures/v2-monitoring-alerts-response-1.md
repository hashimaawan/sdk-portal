# V2 Monitoring Alerts Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2MonitoringAlertsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `policy` | [`Policy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/policy.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.alerts import Alerts
from digitaloceanapi.models.compare import Compare
from digitaloceanapi.models.policy import Policy
from digitaloceanapi.models.slack import Slack
from digitaloceanapi.models.type_17 import Type17
from digitaloceanapi.models.v_2_monitoring_alerts_response_1 import V2MonitoringAlertsResponse1
from digitaloceanapi.models.window_1 import Window1

v_2_monitoring_alerts_response_1 = V2MonitoringAlertsResponse1(
    policy=Policy(
        alerts=Alerts(
            email=[
                'email2',
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
        compare=Compare.GREATERTHAN,
        description='description4',
        enabled=False,
        entities=[
            'entities9'
        ],
        tags=[
            'tags9',
            'tags0',
            'tags1'
        ],
        mtype=Type17.ENUM_V1INSIGHTSDROPLETDISK_READ,
        uuid='uuid0',
        value=149.36,
        window=Window1.ENUM_30M,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



