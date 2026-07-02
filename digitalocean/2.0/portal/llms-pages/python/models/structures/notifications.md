# Notifications

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRk5vdGlmaWNhdGlvbnM

The notification settings for a trigger alert.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Notifications`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `email` | `List[str]` | Required | An email to notify on an alert trigger. |
| `slack` | [`List[Slack]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/slack.md) | Required | Slack integration details. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.notifications import Notifications
from digitaloceanapi.models.slack import Slack

notifications = Notifications(
    email=[
        'bob@example.com'
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
)
```



