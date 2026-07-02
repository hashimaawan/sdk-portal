# Steps of an Alert S Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlN0ZXBzJTI1MjBvZiUyNTIwYW4lMjUyMGFsZXJ0JTI1MjdzJTI1MjBwcm9ncmVzcy4

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`StepsOfAnAlertSProgress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ended_at` | `datetime` | Optional | - |
| `name` | `str` | Optional | - |
| `reason` | [`Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/reason.md) | Optional | - |
| `started_at` | `datetime` | Optional | - |
| `status` | [`Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-2.md) | Optional | **Default**: `"UNKNOWN"` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.reason import Reason
from digitaloceanapi.models.status_2 import Status2
from digitaloceanapi.models.steps_of_an_alert_s_progress import StepsOfAnAlertSProgress

steps_of_an_alert_s_progress = StepsOfAnAlertSProgress(
    ended_at=dateutil.parser.parse('2020-11-19T20:27:18Z'),
    name='example_step',
    reason=Reason(
        code='code2',
        message='message4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    started_at=dateutil.parser.parse('2020-11-19T20:27:18Z'),
    status=Status2.SUCCESS,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



