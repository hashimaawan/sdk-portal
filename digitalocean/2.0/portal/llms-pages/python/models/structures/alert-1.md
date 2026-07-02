# Alert 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkFsZXJ0MQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Alert1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `component_name` | `str` | Optional | - |
| `emails` | `List[str]` | Optional | - |
| `id` | `str` | Optional, Read-only | - |
| `phase` | [`Phase1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/phase-1.md) | Optional | **Default**: `"UNKNOWN"` |
| `progress` | [`Progress2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/progress-2.md) | Optional | - |
| `slack_webhooks` | [`List[SlackWebhooksToSendAlertsTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - |
| `spec` | [`Alert`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/alert.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.alert_1 import Alert1
from digitaloceanapi.models.phase_1 import Phase1
from digitaloceanapi.models.progress_2 import Progress2
from digitaloceanapi.models.reason import Reason
from digitaloceanapi.models.status_2 import Status2
from digitaloceanapi.models.steps_of_an_alert_s_progress import StepsOfAnAlertSProgress

alert_1 = Alert1(
    component_name='backend',
    emails=[
        'sammy@digitalocean.com'
    ],
    id='4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
    phase=Phase1.ACTIVE,
    progress=Progress2(
        steps=[
            StepsOfAnAlertSProgress(
                ended_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                name='name2',
                reason=Reason(
                    code='code2',
                    message='message4',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                started_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                status=Status2.SUCCESS,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            StepsOfAnAlertSProgress(
                ended_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                name='name2',
                reason=Reason(
                    code='code2',
                    message='message4',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                started_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                status=Status2.SUCCESS,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            StepsOfAnAlertSProgress(
                ended_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                name='name2',
                reason=Reason(
                    code='code2',
                    message='message4',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                started_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                status=Status2.SUCCESS,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



