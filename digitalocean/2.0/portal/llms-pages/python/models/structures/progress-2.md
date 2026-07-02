# Progress 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlByb2dyZXNzMg

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Progress2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `steps` | [`List[StepsOfAnAlertSProgress]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/steps-of-an-alert-s-progress.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.progress_2 import Progress2
from digitaloceanapi.models.reason import Reason
from digitaloceanapi.models.status_2 import Status2
from digitaloceanapi.models.steps_of_an_alert_s_progress import StepsOfAnAlertSProgress

progress_2 = Progress2(
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
)
```



