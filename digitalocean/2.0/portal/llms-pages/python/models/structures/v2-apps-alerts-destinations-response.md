# V2 Apps Alerts Destinations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsAlertsDestinationsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alert` | [`Alert1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/alert-1.md) | Optional | - |
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
from digitaloceanapi.models.v_2_apps_alerts_destinations_response import V2AppsAlertsDestinationsResponse

v_2_apps_alerts_destinations_response = V2AppsAlertsDestinationsResponse(
    alert=Alert1(
        component_name='component_name2',
        emails=[
            'emails9'
        ],
        id='id0',
        phase=Phase1.CONFIGURING,
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
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



